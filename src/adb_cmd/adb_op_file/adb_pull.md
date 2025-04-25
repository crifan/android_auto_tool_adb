# adb pull

* 语法
  ```bash
  adb pull <remote_android> [<local_pc>]
  ```
* 含义：将文件从 Android=手机中 复制=拉取 到 电脑端的系统
* 说明
  * `remote_android`是文件或文件夹，都支持
  * 如果没指定`local_pc`的位置，则默认为当前文件夹

## 举例

```bash
adb pull /mnt/sdcard/Download/com.lanyou.bydwj.ikk/ .

adb pull /sdcard/Download/magisk_install_log_2023-08-10T21.59.28.log .

adb pull /sdcard/Download/magisk_patched-27001_YqKbC.img .

adb pull /data/adb/modules/zygisk_lsposed/manager.apk .
```

完整输出效果：

```bash
➜  magisk_kitsuneMask_root adb pull /sdcard/Download/magisk_patched-27001_YqKbC.img .
/sdcard/Download/magisk_patched-27001_YqKbC.img: 1 file pulled, 0 skipped. 35.7 MB/s (67092480 bytes in 1.795s)
```

```bash
➜  LSPosed adb pull /sdcard/Download/magisk_install_log_2023-08-11T09.39.04.log .
/sdcard/Download/magisk_install_log_2023-08-11T09.39.04.log: 1 file pulled, 0 skipped. 0.7 MB/s (4527 bytes in 0.006s)
```

```bash
➜  LSPosed adb pull /sdcard/Download/magisk_log_2023-08-11T09.40.15.log .
/sdcard/Download/magisk_log_2023-08-11T09.40.15.log: 1 file pulled, 0 skipped. 11.3 MB/s (96550 bytes in 0.008s)
```

### 导出整个文件夹

* 用adb导出安卓中的整个文件夹=整个目录
  * 方式1=普通写法：不带点
    ```bash
    adb pull /mnt/sdcard/Download/com.lanyou.bydwj.ikk/ .
    ```
  * 方式2=特殊写法：带点
    ```bash
    adb pull /data/data/com.zhixuan.ancientpoetry/. .
    ```
