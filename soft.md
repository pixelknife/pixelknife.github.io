# 像素刻刀(PixelKnife)软件

像素刻刀软件是处理大型遥感卫星数据特别是中国国产遥感卫星数据的一些重要的软件工具。



## 1 软件功能

软件主要是为了解决实际问题，而且根据2/8原则，力图解决核心问题。

这里主要以高分系类卫星为案例，其他卫星或多或少也有这样一些问题。



### 1.1 高精度配准

可见光RGB波段之间的偏差

多光谱和全色之间的偏差



### 1.2 不失真融合

高分辨率卫星通常采用高空间分辨率的全色和低空间分辨率的多光谱的组合，分辨率上大多数是4倍的关系。需要通过融合算法形成高分辨率多光谱的产品图像。

常用的商业遥感软件的融合算法往往有较大的颜色偏差，导致后续定量化的算法难以开展。



下面利用WorldView3的0.3/1.2米样本数据做了能够做定量化测试的数据集，右边是缩小1/4退化成1.2米/4.8米的输入数据集，左边是1.2米的原始多光谱作为真值来测试算法的误差。

[![f2UZ9J.png](https://z3.ax1x.com/2021/08/15/f2UZ9J.png)](https://imgtu.com/i/f2UZ9J)

下面比较了ENVI的GS、NND、PCI的pansharp以及像素刻刀(pk)的差异。

[![f2YfHO.gif](https://z3.ax1x.com/2021/08/15/f2YfHO.gif)](https://imgtu.com/i/f2YfHO)

[![f2YWDK.gif](https://z3.ax1x.com/2021/08/15/f2YWDK.gif)](https://imgtu.com/i/f2YWDK)

[![f2Ygjx.gif](https://z3.ax1x.com/2021/08/15/f2Ygjx.gif)](https://imgtu.com/i/f2Ygjx)

[![f2YRu6.gif](https://z3.ax1x.com/2021/08/15/f2YRu6.gif)](https://imgtu.com/i/f2YRu6)



### 1.3 缩略图调色

大图像中存在图像亮度和色彩的不均衡，但是因为遥感图像非常大，很难通过photoshop这样的工具来控制颜色。我们的想法是通过建立一个缩略图，然后通过photoshop来调整缩略图的状态，然后通过软件应对到整个大图。



原始图像的缩略图

[![f2aqJg.jpg](https://z3.ax1x.com/2021/08/15/f2aqJg.jpg)](https://imgtu.com/i/f2aqJg)



通过photoshop调色过的

[![f2aLWQ.jpg](https://z3.ax1x.com/2021/08/15/f2aLWQ.jpg)](https://imgtu.com/i/f2aLWQ)



应用到全分辨率图像


[![f2aUG4.gif](https://z3.ax1x.com/2021/08/15/f2aUG4.gif)](https://imgtu.com/i/f2aUG4)



### 1.4 无饱和增强

遥感图像存在局部高亮的区域，可以通过局部的非线性调整，让整个图像中高亮的饱和区域尽可能少。

我们的软件工具可以将调色后失去的高饱和区域的纹理部分恢复回来。

[![f2aaRJ.gif](https://z3.ax1x.com/2021/08/15/f2aaRJ.gif)](https://imgtu.com/i/f2aaRJ)


### 

## 2 软件环境

软件建立在著名的GDAL工具的基础上，包含了最新的GDAL软件功能，并在此基础上增加了新的命令行工具。



## 3 DEMO下载

DEMO版和正式版的差别在于DEMO版上生成的图像中有水印痕迹。


---

**联系方式**

陈甫

中国科学院空天信息创新研究院

chenfu@aircas.ac.cn

13811147935