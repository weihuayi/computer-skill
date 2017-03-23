## Bash 

## LD_PRELOAD

```
export LD_PRELOAD=/usr/lib/openmpi/lib/libmpi.so
```

## 如何更快进入常用文件夹

在 `~/.bashrc` 设置环境变量, 如

```bash
export book=/home/why/repository/why/book
export lecture=/home/why/repository/why/lecture
export research=/home/why/repository/why/research
export whypsc=/home/why/repository/why/whypsc
export pyfem=/home/why/repository/why/pyfem
```
然后命令终端中执行
```
$ source ~/.bashrc
```
或者重启 `bash`. 你就可以在 shell 中输入
```
$ cd $book
$ cd $lecture
$ cd $pyfem
$ cd $research
$ cd $pyfem
```
直接进入常用文件夹了.



## 提高效率的操作技巧

生活在 Bash shell 中，熟记以下快捷键，将极大的提高你的命令行操作效率。

**编辑命令**

快捷键   | 功能 
---------|------------
Ctrl + a | 移到命令行首
Ctrl + e |移到命令行尾
Ctrl + f | 按字符前移（右向）
Ctrl + b | 按字符后移（左向）
Alt + f | 按单词前移（右向）
Alt + b |按单词后移（左向）
Ctrl + xx|在命令行首和光标之间移动
Ctrl + u |从光标处删除至命令行首
Ctrl + k |从光标处删除至命令行尾
Ctrl + w |从光标处删除至字首
Alt + d |从光标处删除至字尾
Ctrl + d |删除光标处的字符
Ctrl + h |删除光标前的字符
Ctrl + y |粘贴至光标后
Alt + c |从光标处更改为首字母大写的单词
Alt + u |从光标处更改为全部大写的单词
Alt + l |从光标处更改为全部小写的单词
Ctrl + t |交换光标处和之前的字符
Alt + t |交换光标处和之前的单词
Alt + Backspace|与 Ctrl + w ~~相同~~类似，分隔符有些差别

**重新执行命令**

快捷键   | 功能 
---------|------------
Ctrl + r|逆向搜索命令历史
Ctrl + g|从历史搜索模式退出
Ctrl + p|历史中的上一条命令
Ctrl + n|历史中的下一条命令
Alt + .|使用上一条命令的最后一个参数

**控制命令**

快捷键   | 功能 
---------|------------
Ctrl + l|清屏
Ctrl + o|执行当前命令，并选择上一条命令
Ctrl + s|阻止屏幕输出
Ctrl + q|允许屏幕输出
Ctrl + c|终止命令
Ctrl + z|挂起命令

**Bang (!) 命令**

快捷键   | 功能 
---------|------------
!! | 执行上一条命令
!blah | 执行最近的以 blah 开头的命令，如 !ls
!blah:p | 仅打印输出，而不执行
!$ | 上一条命令的最后一个参数，与 Alt + . 相同
!^ | 上一条命令的第一个参数
!:n | 上一条命令的第 n 个参数
!$:p | 打印输出 !$ 的内容
!\* | 上一条命令的所有参数
!\*:p |打印输出 !* 的内容
^blah | 删除上一条命令中的 blah
^blah^foo | 将上一条命令中的 blah 替换为 foo
^blah^foo^ | 将上一条命令中所有的 blah 都替换为 foo
