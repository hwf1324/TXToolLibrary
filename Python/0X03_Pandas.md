# 0X03 Pandas

Pandas一般被当作一个轻量级的数据库工具使用.利用它可以轻松完成结构化数据(一般是表格)的读写,合并,切分,索引,排序,填充缺失等处理.虽然它也自带了一些绘图之类的额外功能,但是基本不用.因为实际当中它经常和NumPy,SciPy,matplotlib等模块配合使用.

## 安装

使用pip安装,模块名为pandas.

## CSV读写

对于机器学习初学者来说,pandas最大的用处可能就是读写csv格式(其实pandas也支持别的读写格式).比起自己通过文件读写流来读写数据,用一行pandas调用数据简直爽翻了.

## 数据索引

pandas的DataFrame的索引类似NumPy的矩阵但是索引功能要更加强大.首先pandas的DataFrame每行每列都有标签,可以通过行列的标签名进行索引.其二,DataFrame的索引是可以灵活使用逻辑运算和比较.例如你可以写这种代码:

```python
import pandas as pd
df=pd.DataFrame( {'AAA' : [4,5,6,7], 'BBB' : [10,20,30,40],'CCC' : [100,50,-30,-50]})
df.loc[(df['BBB'] < 25) & (df['CCC'] >= -40), 'AAA']
```

其中的df是一个DataFrame类的对象.

## 数据处理

pandas也有相当的数据处理功能.比起用NumPy自己实现要方便地多.例如填充缺损数据,转换one-hot编码等.这里给出一个转换one-hot编码的例子.

```python
df=pd.DataFrame([['a',12,4],['b',12,2],['a',5,7]])
pd.get_dummies(df)
```

注:做数据处理(例如回归分析)的时候需要把非数字类型的属性转化为数字编码的属性.one-hot就是一种把枚举类型属性转化成若干个布尔类型(或者0-1类型)属性的方法.转化出的属性个数等于转化前属性的选项个数.

## 资料

[Pandas官网](http://pandas.pydata.org/)
[Pandas教程](http://pandas.pydata.org/pandas-docs/stable/cookbook.html)
[(莫烦) Pandas教程](https://morvanzhou.github.io/tutorials/data-manipulation/np-pd/)