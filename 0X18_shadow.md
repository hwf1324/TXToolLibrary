# 0X18 shadow

## 简介

shadow是一款Linux命令行中常用的用户管理工具.用于创建删除修改用户,用户组.

这款软件在Arch Linux的软件库中也属于Core系列,一般的Linux发行版都会自带.如果你的发行版没有安装这个软件包或者你希望升级,那就用包管理软件安装升级.包名为shadow.

## 使用

Linux中用户的各种信息(用户名,密码,登陆shell等)都保存在一些配置文件中.即使没有shadow你也能通过文本编辑来设置用户信息.但是有shadow能让你的生活更美好.需要注意的是,shadow中的很多命令都需要使用者有相应的权限.

`passwd`命令用于修改指定用户的密码.例如Ubuntu系统中,安装系统后第一件事一般就是设置root的密码:

```shell
passwd root
```

`chsh`命令用于修改用户的登陆shell.一般,默认shell是bash,你可以利用这个命令把默认shell改成zsh等你喜欢的shell.

`su`命令用于以指定用户的身份启动一个shell.

`useradd`,`userdel`,`usermod`这三个命令分别用于新建,删除,修改用户.

`groupadd`,`groupdel`,`groupmod`这三个命令分别用于新建,删除,修改用户组.

## 资料

* [shadow官网](http://pkg-shadow.alioth.debian.org/features.php)
* [GitHub上的shadow项目](https://github.com/shadow-maint/shadow)