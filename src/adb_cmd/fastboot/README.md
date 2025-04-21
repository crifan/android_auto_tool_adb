# Fastboot

## 常用 Fastboot 命令

| 命令 | 含义 |
| --- | ---- |
| fastboot devices | 显示（已连接的处于fastboot模式的）安卓设备 |
| fastboot oem unlock | Bootloader解锁（Android 5.0及以下） |
| fastboot oem lock | 恢复Bootloader锁（Android 5.0及以下） |
| fastboot flashing unlock | Bootloader解锁（Android 6.0及以上） |
| fastboot flashing lock | 恢复Bootloader锁（Android 6.0及以上） |
| fastboot flash recovery {filename} | 向安卓设备写入（刷入）文件（内容）|
