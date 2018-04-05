# 0X0D xterm xfce4-terminal

今天要介绍的xterm和xfce4-terminal是两款软件.相互之间没有依赖关系.但是功能设计上有所不同.可以只安装一个,也可以都安装,也可以都不用.

## xterm

xterm是一款基于X Windows System的虚拟终端.它的功能非常简单,就是模拟VT系列终端机.但是它把这个功能做到了极致.VT系列没有的快捷键,它不多加.VT系列支持的功能,它都支持(包括经常被虚拟终端舍弃的ANSI Escape Code).

如果你有什么终端运行的程序有问题(比如快捷键冲突或者显示不正常),不妨用xterm运行试试.

大部分有图形化界面的Linux发行版都会默认安装xterm.如果没有,也可以通过包管理软件来安装.

## xfce4-terminal

xfce4-terminal是xfce4桌面环境中的一个项目.它也是一个虚拟终端.相比xterm,它增加了一些简单的功能(比如工具栏,多标签,剪贴板等).并且个人认为要比xterm好看不少.最最重要的是它和其他xfce4桌面环境组建一样,小巧快速,保持精悍.我是把这个虚拟终端作为我的日常用终端的.

个人感觉这个终端有一个比较坑的地方就是名字太长.你要用命令行启动这个虚拟终端需要完整输入这么一串:

```bash
xfce4-terminal
```

在没有自动补全的情况下尤为痛苦.

## xfce4-terminal下拉终端

xfce4-terminal命令后加参数可以启动下拉式终端:

```bash
xfce4-terminal --drop-down
```

在下拉终端没有启动或者退出之后,第一次调用这个命令会启动下拉式终端.以后调用这个命令不会再次启动另一个下拉式终端,而会重新聚焦到之前启动的那个.

默认情况下,如果下拉式终端失焦就会隐藏(不是退出).

你也可以在xfce4-terminal的设置中,设定下拉式终端的行为.例如默认多次输入启动下来是终端的命令只会重新聚焦的下拉式终端.你可以把它设置为在下拉式终端显示时输入这个命令就隐藏下拉式终端.

配合桌面环境的快捷键设置,就可以得到一键启动下拉式终端的功能.

详情请参看[官方文档](https://docs.xfce.org/apps/terminal/dropdown).

或者[我的教程](https://www.bilibili.com/video/av17715006/).

xfce4-terminal作为xfce4组件中的一员,一般在安装xfce4的时候自动安装.你也可以通过包管理软件单独安装.

## 使用鼠标

虚拟终端是支持鼠标的。例如在xfce4-terminal中使用鼠标左键选中一段文字就可以复制这一段文字。使用鼠标中间点击就能把复制的文件粘贴到指定位置。

## 资料

* [xterm官网](http://invisible-island.net/xterm/)

* [xfce4官网 xfce4-terminal页面](https://docs.xfce.org/apps/terminal/start)