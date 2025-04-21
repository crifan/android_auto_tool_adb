# Can't find service: package

* 现象

```bash
 adb shell pm list packages -f
cmd: Can't find service: package
```

* 原因：缺少su（超级用户）的权限，所以无法运行命令，返回希望的结果
* 解决办法：加上su权限
* 具体步骤
  * 方式1
    ```bash
    adb shell su -c sub_command
    ```
  * 方式2
    ```bash
    adb shell
    su

    sub_command
    ```

## 说明

（1）对于方式1，此处就是：

```bash
adb shell su -c pm list packages -f
```

不过此处特殊，会报错：

```bash
 adb shell su -c pm list packages -f
cmd: Failure calling service package: Failed transaction (2147483646)
```

而加上给shell加上`-t`，即可规避该问题：

```bash
adb shell -t su -c pm list packages -f
```

即可正常输出结果。


注：

相关语法是：

* adb
  * shell
    * `-t: allocate a pty if on a tty (-tt: force pty allocation)`

（2）只有34字节的pm文件：

```bash
blueline:/ # ls -lha /system/bin/pm
-rwxr-xr-x 1 root shell 34 2009-01-01 16:00 /system/bin/pm
```

之前以为是有问题的呢。但其实是正常的，是没有问题的。

此处只是少了权限，没法获取服务，导致报错的。
