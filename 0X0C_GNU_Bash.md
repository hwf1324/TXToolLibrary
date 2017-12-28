# 0X0C GNU Bash

## 简介

bash是一款命令行用户界面（CLI Shell）。它是GNU计划的一部分，这是一款开源、免费的软件。在各种GNU/Linux的发行版中被广泛采用。但是我没有见过把这款Shell用于类Unix以外的系统。

很多初学者学习Linux，首先就要学习bash这个命令行用户界面。所以对于很多半途而废的人来说，“学习Linux”等于“学习bash”。

## 理清概念

这里再次明确一下，Linux是一个系统内核，而bash是一个用户界面。它们是操作系统中的两个组件，就像汽车上的发动机和方向盘。虽然协同合作，但是终究是两码事。你可以在BSD上安装bash，也可以给Linux发行版换其他shell。

另外还需要说明的一点就是命令行界面不等于图形化界面中自带的虚拟终端工具。虚拟终端工具是图形化界面为了兼容命令行程序而提供的一个用于模拟古老的字符终端的窗体程序。但这个虚拟终端里可以用bash，也可以用别的shell。具体而言xterm、Xfce Terminal这些是虚拟终端，bash、dash、csh、ash这些是命令行用户界面。

bash最基本的功能就是解析用户的命令，把它交给内核或者其他程序去执行，有时还要把执行结果以文本形式显示在屏幕上。但是仅仅学会这个还不算完。bash还是一个脚本语言解析器。通过bash脚本，你可以组合各种应用程序完成重复性的劳作。关于bash的使用方式我另有视频和专栏做详细介绍。

## 获取方式

bash一般随发行版安装，并且有内置文档。也可以在GNU计划网站上找到bash的主页,在这个主页查看下载安装的方法。

在Arch库中bash依赖以下包：

* glibc
* ncurses
* readline 需要大于等于7.0版本。

## bash-completion

bash-completion是一个bash的脚本包。用于扩展bash的自动补全功能。

bash自带的自动补全功能一般只能补全命令名、文件名之类的。bash-completion针对许多命令编写了专门的匹配规则。匹配的内容也不再局限于bash自带的命令名、文件名之类的。

以unalias命令为例：

* 在安装bash-completion之前，如果输入unalias命令，然后按TAB键试图补全参数，bash会把当前路径下的文件名作为参数补上。
* 在安装bash-completion之后，输入unalias命令后自动补全参数，就会搜索alias定义的命令别名，用命令别名补全。

如果发行版没有自带这个包，可以通过包管理安装。一般发行版的仓库中都会包含这个包。bash-completion项目托管于Github之上。也可以从Github获取。

## 资料

* [GNU Bash官网](https://www.gnu.org/software/bash/)

* [GitHub上的bash-completion项目](https://github.com/scop/bash-completion)
