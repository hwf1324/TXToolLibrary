# 0001 Python

Python是一门脚本语言.其编译器(解释器)由C语言编写,和C语言有很好的交互性.对比别的依靠解释器或者运行时环境等虚拟机执行的语言,与其说Python是一个增强版的Lua,不如说它是一个简化版的Java.

作为一个比较年轻的语言,在语法设计上,固然要比古老的C/C++这类语言更加优秀(尤其是Python3).但是,很多人,很多项目使用Python的原因主要是:上手快，省心,模块多.另外做数学,算法或者最近很热门的数据挖掘,机器学习等方面工作的人可能会比较青睐这门语言.原因就是它屏蔽了很多底层细节,省心.

个人感觉Python目前的状况很有点像早些年的Java.Java今日的处境可能也是Python以后所要面对的.据说Python最初并不是要设计成一门又大又全的语言,但是它拥有良好的扩展性.随着使用人数和应用领域的增多.Python的各种包各种模块越来越多几乎是不可避免的.很多跨平台跨语言的框架比如OpenCV,QT,dlib等也纷纷给出了Python版本的封装.官方的新版本也不断吸收着各种扩展模块,比如新进被纳入标准库中的tkinetr(一个简单的编写图形化窗体的库).这些固然是好事,但是好事也有另一面--随着扩展的增多,Python变得越来越臃肿了.最直观的感受就是安装完必须的开发环境所需要的磁盘空间越来越多.不过现在就担心Python的解释器变得和Java的JRE一样大还有点早.

由于各种各样的Python模块的存在.你可以用Python来完成很多事情.比如导入个PyQT来做图形化窗体程序,导入个OpenCV的Python版来做图像处理,导入numpy和matplotlib来取代MATLAB的基本功能,导入PyTorch,sklearn或者TensorFlow来做机器学习等等.由于Python自带的包管理pip的存在,这些部署工作现在相对来说都很简单.

需要注意的一点是,Python目前有两个主要版本.一个是旧的Python2,一个是新的Python3.从Python2升级Python3的时候,出于甩掉不合理的最初设计的历史包袱的考虑,Python3不完全兼容Python2.我的建议是最好学习Python3.写新项目都使用Python3.语法,库方面的更新和进步就不说了.一个很重要的原因就是Python2基本上处于停止维护的状态.虽然官方会偶尔修修Bug,但是新特新基本不会往Python2添加了(修Bug也只是为了维持一些老项目,过几年修Bug的工作也可能会停止).

新旧的交替总是需要一点时间.但是我希望Python2不要变成国内计算机课上的VC++6.0.

## 组成和获取

* python

一般直接从Python官网下载官方的发行版就可以。官方发行版还集成了许多实用工具和常用的库。也可以尝试自己从源码编译Python。

在Linux系统中可以使用包管理轻松安装Python。由于存在互不兼容的两个版本，在安装和使用的时候需要区分`python2`和`python3`。

例如在Ubuntu上安装Python3：

```shell
sudo apt install python3
```

## 资料

重新造轮子不一定是一件值得提倡的事.计算机领域更多时候需要分工,合作和共享.有现成的可以利用的成果为什么不用呢.

我目前不打算制作Python的教程,推荐查看官方文档,莫烦的系列Python基础教学以及菜鸟教程中Python相关篇章.

* [Python官网](https://www.python.org/)
* [(莫烦) Python基础教程](https://morvanzhou.github.io/tutorials/python-basic/basic/)
* [(莫烦) Python线程](https://morvanzhou.github.io/tutorials/python-basic/threading/)
* [(莫烦) Python进程](https://morvanzhou.github.io/tutorials/python-basic/multiprocessing/)
* [菜鸟教程 Python3教程](http://www.runoob.com/python3/python3-tutorial.html)

## 信息汇总

* 功能定位：Python语言解释器
* 平台支持：Linux,Mac,Windows
* 开源
* 拓展性：编写C语言模块，Python模块等进行拓展。
* 费用：免费
* 意见：Python常年盘踞在TIOBE前五。就算自己不写Python也难免用到别人写的Python程序。而且数据科学领域使用Python编写的工具非常丰富。可以用Python来替代MATLAB或者Excel。
