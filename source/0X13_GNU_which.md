# 0X13 GNU which

## 简介

which是一个Linux系统中用于定位命令可执行文件位置的工具.一般都是发行版自带.如果没有自带可以使用包管理软件进行安装.

其包名就是`which`.

## 使用

which命令的使用非常简单.就是把要查找的命令作为参数传入.然后就会返回命令可执行文件的完整路径结果.

需要注意的就是它查找的是可执行文件.如果你把ls命令用别名设置为了其他命令.它依旧会查找到可执行文件ls.但是type就仅仅会显示ls是个别名.试比较:

```shell
alias ls='ls -a'
type ls
which ls
```

如果用which搜索的是一个bash内建命令,则which不会有结果.

## 吐槽

只是一个非常简单的小工具.确实Unix的哲学是KISS原则,确实早期的类Unix系统上的工具都是一个一个单独的小工具.但是现在绝大多数小工具都被收录到了GNU coreutils,shadow或者别的什么工具集里.像这样一个还算常用,但是独立成项目(甚至有独立的软件包)的命令非常少见.

最开始写这篇的时候忘了bash还有内置的whereis命令.个人认为type和whereis命令加起来要比which好用.其实没有必要装which.

## 资料

* [GNU which官网](https://savannah.gnu.org/projects/which/)
