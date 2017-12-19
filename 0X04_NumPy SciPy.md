# 0X04 NumPy SciPy

NumPy是一个Python的包.主要提供了张量数据结构,不用循环得批量数据数值运算(比原版更快),以及一些配套的统计,或者数值分析工具函数.它也是很多其他数据分析相关的包的基础.

## 安装

利用pip可以轻松安装这个包:

```bash
pip install numpy
```

有时候可能会提示权限不够,需要再命令前加sudo.

如果pip命令默认版本不是pip3,而你又在使用python3和pip3,这里的"pip"命令就应该换成"pip3".

## 矩阵运算

NumPy提供了矩阵这个类,并且提供了相关的运算.准确来说,NumPy的"array"不是矩阵,而是张量.张量是一个数学概念.单独的纯量(标量)是0阶张量,向量是1阶张量(纯量为元素的向量),矩阵是2阶张量(1阶向量为元素的向量),矩阵为元素的向量是3阶张量...

但是不管怎么说,2阶张量的运算还是我们熟悉的矩阵运算.例如矩阵加减乘除,求逆矩阵,矩阵合并等.在学习这些函数的时候,注意分清元素向运算和矩阵整体运算(例如矩阵乘法和矩阵对应位置元素乘).

利用NumPy的张量数据可以存储大量数据.张量之间的运算就是大规模的数据运算.在张量中索引切片就是对大规模的数据进行索引.张量的元素重排(reshape)就是大规模数据的结构重排.

使用张量比使用Python循环语句要高效,所以一般来说数据分析中尽量把循环语句替换成NumPy的张量运算.

## 工具函数

除了提供张量,张量运算.Numpy还提供了一些专门工具.我认为大致可以分为两类.

一类是编程中比较通用的工具函数,比如排序,二进制文件读写,查看变量类型的函数,查看类型是否可以无损转换的函数等等.这一类工具虽然NumPy提供了,但是不一定做得最好.在实际当中不一定全用得上.比如我很少用NumPy的文件读写,而是经常用Pandas读写数据.

另一类是针对一些数学或者应用数学中常见问题的工具函数,例如金融领域的常见计算,线性代数中的行列式求值和线性方程组求解(numpy.linalg),统计量的计算等等.不过,由于NumPy本身是个偏基础性的模块.它提供的这种功能函数经常不够用.这时候可以用NumPy的拓展模块来补充.

## 函数式编程

由于本人比较关注函数式编程.在这里特别提一句.Python中自带的函数式编程工具有可能和NumPy的张量不兼容.好在NumPy提供了自己的函数式编程工具.具体可以查看NumPy参考手册中的"Functional programming"这章.

## SciPy

SciPy是一个NumPy的拓展包.同样可以通过pip安装(模块名是scipy).

它是包含了常见的数学和物理常数,特殊函数以及一个算法合集.在算法合集中又很多数学问题的现成解决算法.

具体来说,你可以用SciPy计算函数积分数值解(scipy.integrate),求解最优化问题(scipy.optimize),插值运算(scipy.interpolate),计算傅里叶变换(scipy.fftpack),滤波(scipy.signal),矩阵分解(scipy.linalg)等等.

包之间的功能重复肯定是存在的,比如NumPy本身也提供了基本的线性代数运算和傅里叶变换.图像处理我们一般用opencv或者pillow.但是这些包至今并存,是因为各有特色.SciPy和NumPy的功能重复还是很少的,而且据说SciPy算傅里叶变换比NumPy快.

PS:SciPy也是一个组织.他们用NumPy,SciPy,IPython,Jupyter,Pandas,SymPy等搭建了一个Python的科学计算开发环境(或者说工具集).为了区别,称这个组织为SciPy,称那个Python模块为SciPy Library,称这个组织用SciPy Library和其他模块组成的工具集为SciPy ecosystem.

## 数值运算

首先介绍一组概念--"数值运算"和"符号运算".

简单来说,数值运算注重数值解.在精度允许的范围内,允许使用近似值替代精确答案.一些理论上不能求解析解的方程可以用数值解法求近似值.数值运算比较贴近工程实际.

符号运算中往往支持任意精度数(一个int类型可以占用任意个字节,只要需要).运算的对象也不限于复数和实数,而可以是函数,方程或者别的什么东西.这些东西在运算的时候统一表示为'symbol'.在符号运算中工具我们可以化简多项式,求函数积分的解析式等(只要解析式存在,并且可求出).相比之下,符号运算在数学理论研究中用得会比较多.

总体上NumPy和SciPy还是数值运算为主.NumPy加SciPy基本上可以取代MATLAB数值运算模块的功能.这给我们提供了一个MATLAB,Octave之外的解决方案.

## 参考资料

[NumPy官网](http://www.numpy.org/)
[NumPy官方入门教程](https://docs.scipy.org/doc/numpy-dev/user/quickstart.html)
[NumPy参考手册](https://docs.scipy.org/doc/numpy-dev/reference/index.html)
[(莫烦) Numpy教程](https://morvanzhou.github.io/tutorials/data-manipulation/np-pd/)
[SciPy官网](https://scipy.org/index.html)
[SciPy Library](https://scipy.org/scipylib/index.html)
[SciPy参考手册](https://docs.scipy.org/doc/scipy/reference/)
