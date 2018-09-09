# 0012 matplotlib

matplotlib是一个Python的模块,用于绘制图表,展示数据.

## 安装

使用pip安装.包名为matplotlib.

由于涉及图形的显示,部分函数可能需要图形化界面环境和显示器才能正常使用.

## 功能

matplotlib的基本功能是绘制各种二维或者三维的函数图,散点图,云图,直方图,几何图案等.通过调用API可以实现图像标注,颜色,坐标轴,标签,线条样式,字体等方方面面的自定义.

绘制的图像可以通过一个交互式的简单窗体查看(具有放大和拖动功能,需要图形化界面环境和显示器),也可以直接保存成图片文件.

其实你可以使用自定义几何图案的功能绘制几乎任何流程图,示意图.不过更高效的办法是调用matplotlib提供的专门工具包(如果有的话).例如matplotlib自带了绘制雷达图,Sankey图,朗肯循环示意图等的工具.

通过组合静态的图片,matplotlib也能提供一点动画功能(详见matplotlib.animation模块的文档).

此外matplotlib还提供了简单的读取并显示图片文件的工具.

## 注意

在ipython下使用matplotlib.pyplot.show会有一个阻塞的问题(详见这个函数的文档).一个比较常见的坑就是在ipython交互模式下调用show函数,会阻塞ipython,无法进行后续的输入(经过我的测试,python3自带的交互式编程环境没有这个问题).

可以在调用show函数的时候传入参数"block=False"来防止阻塞.例如:

```python
import matplotlib.pyplot as plt
import numpy as np
x = np.linspace(0,10,100)
y = np.sin(x)
plt.plot(x,y)
plt.show(block=False)
```

## 资料

* [matplotlib官网](https://matplotlib.org/)
* [matplotlib官方教程](https://matplotlib.org/tutorials/index.html)
* [(莫烦) matplotlib教程](https://morvanzhou.github.io/tutorials/data-manipulation/plt/)

## 信息汇总

* 功能定位：数据展示，数学绘图，绘图工具库。
* 平台支持： Linux,Mac,Windows
* 开源
* 拓展性：未知
* 费用：免费
* 意见：Python常用的绘图工具库，数据展示工具库。