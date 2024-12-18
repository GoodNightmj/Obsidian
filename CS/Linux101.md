shell 是 Linux 中的一类程序，它可以接受通过键盘输入的命令，然后把命令交给系统执行，并将命令的输出返回给用户。现在几乎所有的 Linux 发行版都提供了一个叫 Bash 的 shell 程序，是传统 shell 的“增强版”。

```
$ # 创建一个文件，名为 FILE_NAME
$ touch FILE_NAME...
```


 使用 tar 操作存档、压缩文件
```
 $ # 命令格式如下，请参考下面的使用样例了解使用方法
$ tar [OPTIONS] FILE...
```


tldr 可用于查看各种指令的大致作用，是man指令的简化板
 ![image.png](https://raw.githubusercontent.com/GoodNightmj/PicGo/master/202411171917933.png)
  sudo !!
  !! 代表上个命令

  `su` 命令用于直接切换用户，格式是 `su 用户名`。如果没有用户名这个参数，则切换到 `root` 用户。
为了更好地理解目录权限的含义，可以把目录视为一个「文件」来看待，这个文件包含了目录中下一层的文件列表——「读取」对应读取文件列表的权限，「写入」对应修改文件列表（添加、删除、重命名文件）的权限，「执行」对应实际去访问列表中文件、以及使用 `cd` 切换当前目录到此目录的权限。



```
/bin 
存储必须的程序文件，对所有用户都可用。
/etc
存储系统和程序的配置文件。
/lib
存放系统运行必须的程序库文件。
/opt
存放额外的程序包。一般将一些大型的、商业的应用程序放置在这个目录。
/usr
大多数软件都会安装在此处。
/var
存储会发生变化的程序相关文件

```

重定向输出 > >>  后者为追加不会更改原本内容

文本处理
wc 统计文本数
diff 比较两个文本内容 
grep 用于查找文本中的指定字符串
sed 用于替换文本中的字符串


与直接执行脚本，或者指定 shell 执行脚本不同，使用 `.` 命令执行脚本会在当前 shell 中执行脚本，而不是新建一个 shell 去执行脚本。这意味着，脚本中的变量定义、函数定义等都会在当前 shell 中生效。
许多 Bash 脚本会在文件首行加上 `#!/bin/bash` 。这里 `#!` 符号的名称是 shebang（也叫 sha-bang，即 sharp `#` 与 bang `!`）。当一个文本文件首行有 shebang，且以可执行模式执行时，shebang 后的内容会看作这个脚本的解释器和相关参数，系统会执行解释器命令，并将脚本文件的路径作为参数传递给该命令。
例如，某个 `foo.sh` 首行为 `#!/bin/bash`，则执行 `./foo.sh` 就等于执行 `/bin/bash ./foo.sh`。
即等同于$ bash show.sh 


可以使用 `export` 命令来定义环境变量。在同一个 shell 中使用 `export` 定义之后，这个环境变量会一直保留，直到这个 shell 退出。







