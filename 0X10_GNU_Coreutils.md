# 0X10 GNU Coreutils

## 简介

Unix系统中有一条叫做“KISS原则”的原则——Keep It Small and Simple.我译为“保持精悍”.也就是说类Unix系统要求其上的软件（尤其是命令行工具）尽量保持短小精悍.一个程序往往只完成很简单的工作.

后来有人为了方便，把很多常用的小工具打包成一个名叫BusyBox的工具集.这个工具集和bash一样成了标准,几乎装Linux系统就自带bash和busybox。后边许多部分所使用的命令其实也是busybox打包的.

再后来GNU计划也出了一个自己的工具集,叫做GNU Core Utilities.包名叫做coreutils.

相比于BusyBox,个人更喜欢使用Core Utilities.因为后者把各种功能分门别类,文档完善,而且定位准确,不会光顾着一次性安装把一些特别大的独立的软件打包进去.

## 主要内容

最初的小工具合集,发展到现在其实已经成了近乎标准的东西.coreutils中的工具几乎都是作为一个操作系统必不可少的.常用的大致有以下几类:

* 基本的文件复制,移动删除操作: cp, mv, rm
* 目录相关: mkdir, ls
* 文件校验: sum, md5sum
* 简单的文本或者流处理工具: cat, sort, echo, tee
* 文件属性修改: chown, chgrp
* 硬盘工具: df, du
* 进程管理: kill

之所以要把这个包单独拿出来介绍是因为正好我的bash教程中要用到.具体的使用方法可以参看官方文档或者我的bash教程.

## 资料

* [GNU Core Utilities官网](https://www.gnu.org/software/coreutils/coreutils.html)
