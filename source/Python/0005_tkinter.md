# 0005 tkinter

## 简介

tkinter也是一个被集成到Python中的模块(可能老版本没有).

这是一个轻量级的图形化窗体程序工具库.虽然比不上pyqt功能丰富但是胜在简单,轻巧和Python内置.如果要写一个简单的交互窗体,用这个工具库还是很方便的.

注意这个工具库的功能需要图形化界面环境才能正常使用.

tkinter和curses不同。curses是一个帮助用户更方便地写CLI程序的接口，而tkinter是用于写GUI的接口。就算curses写出来的程序功能再像GUI程序，由于并不需要X11等图形接口的支持，仍然不能算一般意义上的GUI程序。

## 关于窗体绘制

tkinter的窗体定义方式还是比较传统的调用函数增加控件,通过函数参数控制控件参数的方式.在编写比较大型的交互式界面的时候就比较麻烦,并不像WPF等框架使用描述式文件来描述窗体的样式和布局.

此外tkinter的窗体外观也比较朴实,用于简单的演示或者一般使用还行.但是要想做出一点设计感,或者上点美术效果就很难了.

所以我认为tkinter本身的定位就是配合Python的数据处理之类的功能提供一点简单的图形化交互(比如配合matplotlib做一个交互式的数据展示).也就是说它是给做数据分析之类的非专业编写窗体程序的人用的.如果你想学专门的窗体程序编程,我不建议学Python.视具体平台选择一门合适的技术学习即可.比如Windows平台就用WPF,Linux选择GTK之类的.~~而Android和HTML开发本来就是画界面~~.如果一定要用Python,也请选择pyqt.

## 资料

[官方文档](https://docs.python.org/3/library/tk.html)

[(莫烦) tkinter教程](https://morvanzhou.github.io/tutorials/python-basic/tkinter/)

## 信息汇总

* 功能定位：Python的轻量级GUI接口。
* 平台支持：Linux,Mac,Windows
* 开源
* 拓展性：未知
* 费用：免费
* 意见：如果要写的窗体很简单可以试一试tkinter。如果要写的窗体比较复杂还是选择更加完备的接口和工具比较好。