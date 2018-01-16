# 0X19 util_linux

## 简介

util_linux和busybox, GNU Coreutils等类似,是一个Linux系统上的小工具合集.

它本来是Linux计划的一部分,下载点也由Linux Kernel Organization维护.此外还有一个名为util-linux-ng的分支版本.

这个工具集中曾经有也有很多命令,但是目前的处境非常尴尬.它有大量功能和busybox, GNU Coreutils, shadow, systemd等工具集重复,没有自己的特色.而为了降低重复,它在2015年又移除了包括arch, halt, reboot等的一系列命令.

就我用得到的范围来说,目前只有这几个命令是util_linux提供,而其GNU Coreutil, shadow, systemd都没有提供的:

```shell
cal
```

这个命令的作用是查看日历,可以加参数指定查看的年月.

```shell
cal
```

还有mount和umount用于挂载存储器和卸载挂载的存储器.

## 安装

Linux发行版一般会自带这个工具包.在Arch的包管理库中这个工具包的名称就是util-linux.但我很怀疑会有人用包管理软件去装这个.

## 资料

* [GitHub上的util-linux项目](https://github.com/karelzak/util-linux)
* [Wikipedia util-linux](https://en.wikipedia.org/wiki/Util-linux)
* [Linux官方提供的下载源](https://www.kernel.org/pub/linux/utils/util-linux/)