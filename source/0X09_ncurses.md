# 0X09 ncurses, curses

## 简介

curses library是一个在字符终端下编写交互界面的工具包.它可以用符号,前景色背景色拼接出窗口,按钮,菜单,输入框等控件的样子.而使用这个工具的时候则不需要操心printf语句或者ANSI Escape Code的问题.只需要像写图形化界面下的窗体程序一样,定义按钮坐标和内容,菜单位置和选项之类的东西就行了.现在的Linux系统中一般安装的是被称为“new curses”的ncurses。

## 相关命令

ncurses主要是一个被其他程序依赖的库。不过它也提供了几个简单的命令。例如常用的`clear`清空屏幕命令就是ncurses提供的。

### 使用效果

Python官网上有一个用curses写的[康威的生命游戏](https://en.wikipedia.org/wiki/Conway%27s_Game_of_Life)的[demo](https://github.com/python/cpython/blob/3.6/Tools/demo/life.py).

![康威的生命游戏](./images/康威的生命游戏.png)

而用它构建出来的伪图形化界面则像是这样:

![curses.jpg](./images/curses.jpg)

## 资料

[ncurses](http://invisible-island.net/ncurses/ncurses.html)
