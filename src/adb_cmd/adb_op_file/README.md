# adb管理文件

* adb管理文件
  * 从PC端=电脑端 下载=推送 到 安卓端=Android手机中
    ```bash
    adb push <local_pc> <remote_android>
    ```
  * 将文件从 Android=手机中 复制=拉取 到 电脑端的系统
    ```bash
    adb pull <remote_android> [<local_pc>]
    ```
    * 说明
      * 如果没指定`local_pc`的位置，则默认为当前文件夹
