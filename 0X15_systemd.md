# 0X15 systemd

## 简介

systemd是Linux系统中的一个基础模块.它提供了一个系统和服务管理器.一般这个管理器的PID为1,并且负责启动系统的其他部分.

虽然说开源世界的系统中,连系统内核都有多种选择(linux,bsd,hurd).但是我实在是没有见过有Linux发行版不安装systemd的.也没试过在没有安装systemd的系统上安装systemd.不过这里还是给出Arch Linux中systemd的软件包名--'systemd'.

## 命令

介绍这个软件并不是要深入讨论Linux的启动原理.而是因为我的bash教程刚好做到了进程管理这一块,涉及到了几个来自systemd的命令.

首先就是shutdown命令.用于关机.加上参数`now`可以立即关机.

```shell
shutdown now
```

其实这个`now`也可以是别的参数,用于设置延时关机--在一段时间之后关机.

然后是reboot,halt和poweroff.

## WSL

在WSL(Windows Subsystem for Linux)上,systemd并没有被完整支持.所以在子系统中用shutdown,reboot之类的命令一般是没法正常工作的.因为WSL是一个Windows的子系统,它并不是自己独立引导的.

## 资料

* [GitHub上的systemd项目](https://github.com/systemd/systemd)
* [systemd wiki](https://www.freedesktop.org/wiki/Software/systemd/)
* [Arch Linux关于systemd的wiki页面](https://wiki.archlinux.org/index.php/Systemd)
* [Ubuntu关于systemd的wiki页面](https://wiki.ubuntu.com/systemd)
