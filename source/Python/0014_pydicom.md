# 0014 pydicom

## DICOM影像和pydicom

DICOM全称“Digital Imaging and Communications in Medicine”，是传输、存储、恢复、打印、处理和展示医学影像信息的国际标准。简单来说它是医学影像界通用的文件格式。

DICOM文件常见的文件后缀名是“dcm”。但是也有的软件生成DICOM文件的时候不带有后缀名。

而pydicom是Python的一个用于读取和处理DICOM格式文件的工具包。要安装这个工具包使用pip命令：

```shell
pip install pydicom
```

## 测试和练习

如果手头没有DICOM格式的数据，你可以先使用pydicom内置的测试数据做一些基础练习。

首先是导入所需要的包：

```python
import pydicom
from pydicom.data import get_testdata_files
```

其中的`get_testdata_files`是用于获取测试数据路径的函数。使用这个函数获取数据路径然后用`dcmread`函数读取DICOM文件。注意`get_testdata_files`返回的是一个字符串数组，而`dcmread`接受的参数为一个字符串。

```python
FILENAME = get_testdata_files("rtplan.dcm")[0]
DS = pydicom.dcmread(FILENAME)
```

完成读取后变量`DS`就是读取到的文件内容。这实际上是一个字典型的数据结构由若干键值对组成。但是它的`type`却不是Python自带的字典数据结构，而是由pydicom定义的一种字典数据结构。使用

```python
print(DS)
```

可以浏览`DS`的大致内容。使用

```python
print(DS.dir())
```

可以查看`DS`中所有键值对的键。`dir`函数也可以接受一个字符串作为参数，这样它会返回所有带有这个字符串的键。例如：

```python
print(DS.dir("Patient"))
```

如果要访问一个键对应的值，一般使用语法糖，把键当作`DS`的成员来访问。例如：

```python
print(DS.PatientName)
```

（其中`PatientName`就是一个键。）

更多相关内容参见pydicom的`pydicom.dataset.FileDataset`等章节。

## 图象和显示

附加有图象数据的DICOM一般会带有一个名为`PixelData`的键。刚刚我们使用的那个测试数据并没有`PixelData`，我们需要重新导入一个带图象数据的。

```python
FILENAME2 = get_testdata_files("MR_small.dcm")[0]
DS2 = pydicom.dcmread(FILENAME2)
```

我们来看一下图象数据的内容和图像大小：

```python
print(DS2.PixelData)
```

如果你使用Numpy，那么可以通过这个属性访问矩阵形式的图片：

```python
print(DS2.pixel_array)
print(DS2.pixel_array.shape)
```

有了矩阵形式的图象，要显示就和其他矩阵形式的图片类似了。通过matplotlib可以绘制图象

```python
import matplotlib.pyplot as plt
plt.imshow(DS2.pixel_array, cmap=plt.cm.bone)
plt.show()
```

## 真实数据

要是使用真实数据，只要把`FILENAME`换成你要读取的DICOM文件的路径就可以了。

但是注意DICOM的几种存储方式。对于比较简单的情况，一张图片（及其附加的一些文字数据）用一个DICOM文件存储。而成系列的CT图象，或者病人病史，多个病人的影像档案等，则会使用有组织的分层存储方式。

在分层存储中，会有一些不存储图象，仅仅存储目录信息的名为“DICOMDIR”的文件。通过文件目录和DICOMDIR文件，可以建立起一个树状的结构。在读取这类型的文件（或者文件夹）时应当先读取作为根的DICOMDIR文件。根据里边的信息去查找各个枝干的图片或者其他文件。

这里有一篇博客对此做了介绍：<https://blog.csdn.net/Angle_Cal/article/details/78594839>

对于处理分层存储的DICOM文件，pydicom手册上也给出了一个示例程序：<https://pydicom.github.io/pydicom/stable/auto_examples/input_output/plot_read_dicom_directory.html>。

## 参考资料

* [DICOM wikipedia](https://en.wikipedia.org/wiki/DICOM)
* [DICOM标准官网](https://www.dicomstandard.org/)
* [pydicom的PyPI主页](https://pypi.org/project/pydicom/)
* [pydicom的使用手册](https://pydicom.github.io/pydicom/stable/getting_started.html)