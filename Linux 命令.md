## Linux 命令

在 Linux 中，`~` 表示的是 `root` 目录



显示行号：窗口输入 **set number**

取消显示行号：窗口输入 **set nonumber**



查看当前目录下的文件，只显示名字：**ls**

查看当前目录下的文件，显示每个文件/文件夹的详细信息：**ll = ls -l**

查看当前目录下的文件，包括隐藏文件，只显示名字：**ls -a**

查看当前目录下的文件，包括隐藏文件，显示每个文件/文件夹的详细信息：：**ll -a**



查看某个目录下的树形结构：**tree [文件夹]**

```shell
[root@VM-219-139-centos /oy]# tree /oy
/oy
├── docker-compose
├── dockerfile
│   └── Dockerfile
├── enable_internet_proxy.sh
├── ft_local
├── go
│   ├── download
│   └── work
│       ├── bin
│       ├── pkg
│       └── src
│           └── helloworld
│               └── Helloworld.go
└── vsftp_install.sh
```



创建文件夹：**mkdir [文件夹1] [文件夹2]**

递归创建文件夹： **mkdirs [文件夹目录]**



vim 撤销当前操纵：**u**		 （类似 ctrl + z）

vim 撤销撤销操作：**ctrl + r**（类似 ctrl + y）



vim 删除当前行 **dd**



vim 跳到开头：**gg**

vim 跳到结尾：**shift + g**



vim 中文乱码设置：

1. 执行 `echo $LANG` 命令发现输出 `C`，表示是语言环境没有设置好
2. 执行 `vim /etc/profile`，在末尾添加 `export LANG="en_US.UTF-8" `
3. 添加完成 `wq` 退出，执行 `source /etc/profile` 即可
4. 再次执行 `echo $LANG`，输出 `en_US.UTF-8` 即设置完毕



文件移动：**mv 【源文件】 【目标文件】**

```
它是将源文件拷贝一份到目标文件的位置，然后将这个文件重命名为目标文件名，然后再删除掉源文件
```

文件夹移动：**mv 【源文件夹】 【目标文件夹】**

```
如果目标文件夹存在，那么将源文件夹移动到目标文件夹下面
如果目标文件夹不存在，那么将源文件夹改名为目标文件夹(最多只能最后一级文件夹不存在，否则显示 No such file or directory)
```



文件/文件夹拷贝：**cp -r【源文件/源文件夹】【目标文件/目标文件夹】**

```
-r 表示拷贝文件夹下所有的文件/文件夹，这个参数对文件拷贝没有意义，不过加了也没问题
cp 拷贝如果文件/文件夹不存在那么会进行创建
```



解压 rar 文件到当前文件夹：**rar x [rar文件]**



查看占用端口的进程：**netstat -tunlp|grep 【端口号】**



查看所有进程： **ps -a**

查看与本次登陆有关的进程：**ps -l**

正则匹配某个进程信息：**ps -aux | grep 【部分进程名】**



查看 CPU、内存、进程的动态信息：**top**（ps 查看的是进程的信息快照）



强制杀死进程：**kill -9**（通过发送信号的方式）

通知进程关闭：**kill -15**（通过发送信号的方式，非强制，进程可以选择关闭或者不关闭）
