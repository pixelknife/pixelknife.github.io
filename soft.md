# 像素刻刀(PixelKnife)软件

像素刻刀软件是处理大型遥感卫星数据特别是中国国产遥感卫星数据的一些重要的软件工具。



## 1 软件功能

软件主要是为了解决实际问题，而且根据2/8原则，力图解决核心问题。

这里主要以高分系类卫星为案例，其他卫星或多或少也有这样一些问题。



### 1.1 高精度配准

处理高分卫星数据时首先要处理可见光RGB波段之间的偏差、多光谱和全色之间的偏差。

以一景GF2为例

分发的数据集中全色和多光谱之间，右半边不动，左半边有明显偏差
[![f264yD.gif](https://z3.ax1x.com/2021/08/15/f264yD.gif)](https://imgtu.com/i/f264yD)

如果不配准直接融合，会导致严重的模糊和失真
[![f265Oe.gif](https://z3.ax1x.com/2021/08/15/f265Oe.gif)](https://imgtu.com/i/f265Oe)

基于梯度场的非线性几何配准后，误差应该低于0.1像元
[![f26hQO.gif](https://z3.ax1x.com/2021/08/15/f26hQO.gif)](https://imgtu.com/i/f26hQO)

调整前后的多光谱的位移
[![f26oeH.gif](https://z3.ax1x.com/2021/08/15/f26oeH.gif)](https://imgtu.com/i/f26oeH)



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

实际应用PixelKnife处理GF2，融合前后的多光谱的波谱差异很小。
[![f26Twd.gif](https://z3.ax1x.com/2021/08/15/f26Twd.gif)](https://imgtu.com/i/f26Twd)



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




## 2 配置环境

### 硬件环境

内存是一个关键要求：**电脑需具备16GB内存**。
适当注意硬盘空间：每个GF1融合复原结果为3GB，每个GF2融合复原结果为8GB。
估计执行时间（在普通PC或笔记本）：GF1一景5分钟、GF2一景15分钟。

实际测试用例：
电脑配置：windows 7 64位系统  intel core i7-6700 @3.4GHz  内存16GB
GF1： 263秒
GF2： 813秒

### 软件环境

本软件在64位的WINDOWS系统上工作，需要vs2013的runtime运行库。
本软件是绿色软件，即不需要复杂的安装卸载步骤，用户只需要将安装包直接解压在指定的位置即可。



## 3 DEMO下载

DEMO版和正式版的差别在于DEMO版上生成的图像中有水印痕迹。

PixelKnife的DEMO版，从FTP下载
服务器：  satsee.ceode.ac.cn
账号：  cfdata
密码：  cfdata123
个别FTP客户端可能链接不上，推荐使用FTPRush

其中vcredist_x64.exe是vs2013的运行库安装包。
其中pkDemo.zip是软件压缩包。
bj_gf目录中有北京范围的高分一号和高分二号样本各一景。**高分二号这景是2015年9月3日11时36分，纪念中国人民抗日战争暨世界反法西斯战争胜利70周年大阅兵的抓拍，非常值得珍藏。**后面的例子也是用的这景图像。




---

**联系方式**

陈甫

中国科学院空天信息创新研究院

chenfu@aircas.ac.cn

13811147935