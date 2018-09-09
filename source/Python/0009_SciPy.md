# 0009 SciPy

SciPy是一个NumPy的拓展包.同样可以通过pip安装(模块名是scipy).

它是包含了常见的数学和物理常数,特殊函数以及一个算法合集.在算法合集中又很多数学问题的现成解决算法.

具体来说,你可以用SciPy计算函数积分数值解(scipy.integrate),求解最优化问题(scipy.optimize),插值运算(scipy.interpolate),计算傅里叶变换(scipy.fftpack),滤波(scipy.signal),矩阵分解(scipy.linalg)等等.

包之间的功能重复肯定是存在的,比如NumPy本身也提供了基本的线性代数运算和傅里叶变换.图像处理我们一般用opencv或者pillow.但是这些包至今并存,是因为各有特色.SciPy和NumPy的功能重复还是很少的,而且据说SciPy算傅里叶变换比NumPy快.

PS:SciPy也是一个组织.他们用NumPy,SciPy,IPython,Jupyter,Pandas,SymPy等搭建了一个Python的科学计算开发环境(或者说工具集).为了区别,称这个组织为SciPy,称那个Python模块为SciPy Library,称这个组织用SciPy Library和其他模块组成的工具集为SciPy ecosystem.

## 资料

* [SciPy官网](https://scipy.org/index.html)
* [SciPy Library](https://scipy.org/scipylib/index.html)
* [SciPy参考手册](https://docs.scipy.org/doc/scipy/reference/)
* [CSDN上的一篇教程](https://blog.csdn.net/q583501947/article/details/76735870)

## 信息汇总

* 功能定位：科学计算工具包（傅里叶变换，优化，插值，统计等）。提供常用函数，特殊函数，常见数学常数，常见物理常数等。
* 平台支持：Linux,Mac,Windows
* 开源
* 拓展性：未知
* 费用：免费
* 意见：一个基于NumPy的科学计算工具包。如果用到其中的功能可以试一试。
