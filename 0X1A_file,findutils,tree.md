# 0X1A file, findutils, tree

这一期介绍三个用于命令行的文件管理工具。

## tree

tree是一个单独的软件包。其中最主要的就一个`tree`命令。这个命令的作用是递归遍历指定路径的所有子路径然后绘制一张树状图。例如:

```shell
tree /home
```

* [tree命令官网](http://mama.indstate.edu/users/ice/tree/)

## file

file命令也是一个独立软件包。其中的`file`命令的作用是判断指定文件的文件类型。

例如:

```shell
file /bin/bash
file test.c
```

* [file命令官网](https://www.darwinsys.com/file/)

## findutils

findutils和coreutils一样是GNU计划推出的一个基本工具集。这个工具集的主要用途就是文件搜索。

find命令用于在一个目录中搜索文件名。

locate则是在数据库中进行搜索。

find和locate的区别详见findutils的手册。

此外一个标准输入输出流工具xargs也被归入这个工具集。主要是让一些本来不支持标准输入流，或者标准输出流的工具也能融入到流式处理中。例如ls不支持标准输入流。所以这种写法并不能用`ls`列出/bin文件夹里全部内容：

```shell
echo /bin | ls
```

但是使用xargs可以让ls在标准输入流环境中工作。例如：

```shell
echo /bin | xargs ls
```

以上的命令看起来是脱裤子放屁。但是xargs和find，locate组合起来使用就强大了。比如定位所有名字中带bin的文件然后用ls查看其中的文件夹的内容：

```shell
locate  bin | xargs ls
```

* [findutils官网](https://www.gnu.org/software/findutils/)