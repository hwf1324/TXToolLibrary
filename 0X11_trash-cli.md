# 0X11 trash-cli

## 简介

Linux常用GNU Coreutils中提供的命令来管理文件.但是其中的rm命令删除文件后一般无法恢复.这样就很容易因为误操作而造成数据损失.

因而一般不推荐使用rm命令.我们需要一个更加安全的删除命令.

trash-cli就是是一款Linux命令行中使用的安全版的文件删除命令.其机制类似于Windows下的回收站.使用trash删除的文件或者目录会进入一个缓冲目录(垃圾桶).当过一段时间,你确认没有删错文件之后,可以再清空垃圾桶以释放硬盘空间.

## 安装

可以使用包管理软件直接安装.包名是trash-cli.但是Ubuntu上安装的版本比较旧,不知道为什么缺少一个trash-restore命令.所以我还是建议源码安装.

## 基本使用

```shell
trash-put test
```

把test移动到垃圾桶.这里的test可以是文件也可以是目录.一般我会用别名'trash'来替代trash-put命令.

被移动到垃圾桶的文件不会被ls显示,也无法cd或者做别的操作.但是可以实用trash-list命令查看垃圾桶中文件的信息.

使用trash-restore命令可以查看可以恢复的文件序号,然后输入要恢复的文件序号就会恢复目标文件.另外trash-restore命令一般会优先显示从当前目录下删除的文件.

使用trash-empty命令可以清空垃圾桶中的全部文件.

使用tarsh-rm可以仅仅彻底删除垃圾桶中的指定文件.例如:

```shell
trash-rm test
```

## 资料

* [GitHub上的trash-cli项目](https://github.com/andreafrancia/trash-cli)
