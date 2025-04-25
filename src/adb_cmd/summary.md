# adb常用命令概述

| 命令 | 说明 |
| --- | ---- |
| adb devices | 显示所有连接的 adb 兼容设备 |
| adb push &lt;local_pc&gt; &lt;remote_android&gt; | 将文件从 电脑端 复制=下载到Android手机的位置 |
| adb pull &lt;remote_android&gt; [&lt;local_pc&gt;] | 将文件从 Android 复制到电脑端的系统；如果没指定`local_pc`的位置，则默认为当前文件夹 |
| adb install &lt;app_file.apk&gt; | 将应用程序从系统的 apk 文件位置安装到 Android 设备上 |
| adb uninstall &lt;app_package_name&gt; | （通过app的包名）卸载安卓app |
| adb backup | 备份 Android 设备 |
| adb connect | 通过 WiFi 网络使用adb命令 |
| adb shell screencap | 获取设备的屏幕截图 |
| adb reboot | 在正常模式下，重新启动 Android 手机 |
| adb reboot bootloader | 启动设备（以）进入`Fastboot`模式 |
| adb logcat | 实时查看logcat日志信息：（1）查看radio日志：`adb logcat -b radio`（2）以彩色模式查看：`adb logcat -C` |
