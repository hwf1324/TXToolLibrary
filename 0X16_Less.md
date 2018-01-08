# 0X16 Less

## 简介

Less是一款Linux字符终端下查看纯文本文件的工具.它没有任何的编辑功能,仅仅是查看.所以从功能上来说比vi还要精简.

Less也有一些同类软件(例如more),但是个人认为还是Less比较好用.所以这里只介绍Less.

一般的Linux发行版中会自带Less.如果没有自带的话可以通过包管理软件安装,包名是less.

## 使用

Less的命令非常简单,就是less,后接要阅读的文件名.例如:

```shell
less readme.txt
```

如果给与的文件不是一个标准的文本文件(例如故意输入一个二进制文件的路径),那么less也会按照文本文件来解析显示.

进入阅读界面后,使用方向移动.左右方向键用于左右移动,上下方向键用于上下移动,PageUp和PageDown用于上下翻页.Home和End则用于定位到文首,文尾.

如果不想使用PageUp和PageDown,也可以使用空格向下翻页,用b键向上翻页.

按h键打开帮助信息.

除了直接读取文件,Less也接受流输入.例如:

```shell
ls | less
```

```shell
man bash | less
```

顺便提一下,man-db是依赖less的.

## 资料

* [Less官网](http://www.greenwoodsoftware.com/less/)