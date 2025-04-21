# 查看包名

* 语法
  ```bash
  adb shell -t su -c pm list packages -f | grep xxx
  ```

## 举例

通过adb中pm子命令：

```bash
 adb shell -t su -c pm list packages -f | grep youtube
package:/data/app/com.google.android.youtube-m4SwdJhBnwzgDJL3JmRFLA==/base.apk=com.google.android.youtube
```

查看到了YouTube的包名是：

* `com.google.android.youtube`
