# adb安装apk

* 语法
  ```bash
  adb install xxx.apk
  ```
  * == `adb push xxx.apk somePath` + `pm install /somePath/xxx.apk`

## 举例

```bash
crifan@licrifandeMacBook-Pro  ~/dev/dev_tool/android/EdXposed  pwd
/Users/crifan/dev/dev_tool/android/EdXposed
 crifan@licrifandeMacBook-Pro  ~/dev/dev_tool/android/EdXposed  ll
total 8224
 crifan@licrifandeMacBook-Pro  ~/dev/dev_tool/android/EdXposed  adb install EdXposedManager-4.6.2-46200-org.meowcat.edxposed.manager-release.apk
Performing Streamed Install
Success
```
