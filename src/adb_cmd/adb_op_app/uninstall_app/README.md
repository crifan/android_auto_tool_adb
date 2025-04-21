# adb卸载app

* 语法
  * 最精简
    ```bash
    adb uninstall <app_package>
    ```
  * 用shell
    ```bash
    adb shell pm uninstall <app_package>
    ```
    * 等价于
      ```bash
      adb shell
      su
      pm uninstall <app_package>
      ```
  * 加其他参数
    * `-k`
      ```bash
      pm uninstall -k --user 0 <app_package>
      ```

## 举例

```bash
adb uninstall com.google.android.youtube

pm uninstall -k --user 0 com.google.android.youtube

adb uninstall com.google.android.gms

adb shell pm uninstall com.example.MyApp

adb shell
su
pm uninstall com.google.android.youtube
```

### 部分输出

```bash
blueline:/ # pm uninstall com.google.android.youtube
pm uninstall com.google.android.youtube
Success
```

```bash
blueline:/ # pm uninstall -k --user 0 com.google.android.youtube
pm uninstall -k --user 0 com.google.android.youtube
Success
```

```bash
➜  ~ adb uninstall com.google.android.gms
Success
```
