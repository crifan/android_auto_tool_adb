# adb push

* 语法
  ```bash
  adb push <local_pc> <remote_android>

  adb push /src/pc/side//file_or_folder /dest/android/side/file_or_foler
  ```
* 含义：从PC端=电脑端 下载=推送 到 安卓端=Android手机中

# 举例

```bash
adb push boot.img /sdcard/Download/boot.img

adb push boot.img /sdcard/Download
adb push riru-v25.4.4-debug.zip /sdcard/Download
adb push Magisk-v26.1.apk /sdcard/Download/
adb push LSPosed-v1.8.6-6712-zygisk-release.zip /sdcard/Download/
adb push Shamiko-v0.7.3-174-release.zip /sdcard/Download/

adb push F:\drizzleDumper /data/local/tmp

adb push lldb-3.1.4508709-linux-x86_64/android/arm64-v8a/lldb-server /data/local/tmp
```

完整效果：

```bash
➜  lineage-19.1-20241110-UNOFFICIAL-dipper adb push boot.img /sdcard/Download/
boot.img: 1 file pushed, 0 skipped. 106.8 MB/s (67092480 bytes in 0.599s)
```

```bash
➜  LSPosed adb push LSPosed-v1.8.6-6712-zygisk-release.zip /sdcard/Download/
LSPosed-v1.8.6-6712-zygisk-release.zip: 1 file pushed, 0 skipped. 53.5 MB/s (2362560 bytes in 0.042s)
```

```bash
➜  LSPosed adb push Shamiko-v0.7.3-174-release.zip /sdcard/Download/
Shamiko-v0.7.3-174-release.zip: 1 file pushed, 0 skipped. 327.6 MB/s (247141 bytes in 0.001s)
```
