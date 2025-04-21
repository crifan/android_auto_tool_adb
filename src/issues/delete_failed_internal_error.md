# Failure DELETE_FAILED_INTERNAL_ERROR

* 现象

```bash
pm uninstall com.google.android.youtube
```

报错：

`Failure [DELETE_FAILED_INTERNAL_ERROR]`

其实是，很可能是：

要删的app已经被删了

所以再去删除，才报错的

* 解决办法：无需解决
* 相关说明
  * 想要搞清楚，是否是：该app是已经删除过了，可以通过：
    ```bash
    pm list packages -f | grep youtube
    ```
    * 查看和确保，app：
      * 当前是否还在
      * 还是：是否不在了，已经被删了
  * 另外：如果已经被删了，则：
    ```bash
    adb shell -t su -c pm uninstall -k --user 0 com.google.android.youtube
    ```
    * 会输出有价值的提示的：
      * `Failure [not installed for 0]`
      * 含义：表示该app没有安装==已被删除
        * 解释
          * not installed for 0
            * `0`指的是：`--user 0` == root用户
              * 对于root用户，没有安装该app

