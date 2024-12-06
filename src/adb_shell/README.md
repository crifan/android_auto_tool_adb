# adb shell

## 命令提示符

`adb shell`进入shell后：

* 命令行提示符
  * `#`=`井号`：`root`用户
  * `$`=`美元`符号：`普通`用户

另外，也可以通过：

```bash
whoami
```

查看当前用户是什么

举例：

* root用户

```bash
blueline:/ # whoami
root
```

* 普通用户：`shell`

```bash
13|blueline:/ $ whoami
shell
```

## adb shell命令行前面的数字

正常情况，shell前面是没有数字的：

```bash
 adb shell
blueline:/ # pwd
/
```

但是，如果前面出现一个数字加上竖杠，则表示：前一次命令执行的返回值，前一个命令运行出错了的出错码

比如：

```bash
blueline:/ # pm --help
cmd: Can't find service: package
20|blueline:/ #
```

此处的 `20|` 就是`前一个命令运行出错的返回值`=`出错码`

而继续运行，如果后续命令正常运行，则出错码就消失了：

```bash
20|blueline:/ # which pm
/system/bin/pm
blueline:/ #
```

其实表示的是：

* 上一个命令运行结果=返回值
  * `0`：表示没有出错
    * 所以就不显示出错码
  * `非0`：就显示，提示你出错了

![adb_shell_prefix_number](../assets/img/adb_shell_prefix_number.png)
