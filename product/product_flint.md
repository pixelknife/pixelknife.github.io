# 火石夜光产品



欢迎访问“火石”地球夜光产品！“火石（Flint）”是由中国科学院空天信息创新研究院陈甫团队研制的地球夜光产品数据集。目前在新华社媒体融合生产技术与系统国家重点实验室的资助下，成为其新华地球系统的一部分，继续更新处理算法，发布新的版本。

它是在[美国科罗拉多矿业大学](https://eogdata.mines.edu/products/vnl/)发布的NPP卫星VIIRS传感器的夜光月度产品的基础上进一步加工而成。相对于原有的产品，火石(Flint)提供更高的准确性、稳定性、易用性。它可以用来持续地跟踪地球表面的人类活动。

想了解它的来龙去脉可以点击我们在科普中国上刊登的[科普文章](http://www.kepuchina.cn/wiki/yzts/201805/t20180518_629897.shtml)。

## 1 数据访问

目前我们最新提供的是Flint2.0 beta版的产品（2021年出品），现在可以通过WebGIS提供中国周边区域的查询和展示服务。2.0版本在1.0版的基础上，增强了产品图像清晰度和数值绝对值的稳定性。

A) 年度时序(2012-2020)，这里将亮度灰度图渲染为认可度更高的黄色

[http://satsee.radi.ac.cn/cfdata/doc/flint/year_sharp_yellow/](http://satsee.radi.ac.cn/cfdata/doc/flint/year_sharp_yellow/)

<center>
<video width="640" controls="controls" loop="loop" autoplay="autoplay">
  <source src="flint_yellow.mp4" type="video/mp4" />
Your browser does not support the video tag.
</video>
</center>

B) 年度变化时序(2013-2020)，橘色是变亮的区域，蓝色是变暗的区域，灰色是不变的区域，后面叠加了谷歌地球的底图作为参考。

[http://satsee.radi.ac.cn/cfdata/doc/flint/year_chg/](http://satsee.radi.ac.cn/cfdata/doc/flint/year_chg/)

<center>
<video width="640" controls="controls" loop="loop" autoplay="autoplay">
  <source src="flint_chg.mp4" type="video/mp4" />
Your browser does not support the video tag.
</video>
</center>



## 2 Flint的意义

下面的北京、天津地区的动画表达了Flint月度产品和原版的差异，上半部分是Flint制作的月度变化时序，下半部分是美国原版的内容。

<center>
<video width="640" controls="controls" loop="loop" autoplay="autoplay">
  <source src="beijing.mp4" type="video/mp4" />
Your browser does not support the video tag.
</video>
</center>


可以看到原版的月度产品两期之间普遍存在波动，而且随着纬度提高（大致上海以北），因为昼夜长短变化会导致个别月份没有数据。

Flint版在原版的基础上进一步加工，使月度之间基本数值保持高度稳定，月度之间的实质性变化因此可以更加明确、更加突出。在此基础上可以定制季度产品或者年度产品，这样相邻两期之间的变化更大，更容易识别。

## 3 突变和渐变

夜光变化可以在概念上分成小区域的突变和大区域的渐变两种，后者容易和观测条件（气象条件）产生的非实质性偏差混淆，需要更长时间（超过气象影响周期）的观测才能确定。所以定量化的分析还是很有挑战性。

上面中国北京的例子有很明显的小区域突变，但是很难看到大区域的渐变，而这在印度却很常见，甚至是主要的变化模式。

印度新德里位于印度北部平原上东西两个邦之间。下面这个年度时序（取每年第12月为代表）表明印度的夜光整体波动较大，而且和邦的行政区划很一致。我认为这和印度的电力生产和管理的能力有很大的关系。

<center>
<video width="640" controls="controls" loop="loop" autoplay="autoplay">
  <source src="newdelhi2.mp4" type="video/mp4" />
Your browser does not support the video tag.
</video>
</center>

可以通过彩色增强来突出表达年度之间的变化，橘色是增强，蓝色是减弱。

<center>
<video width="640" controls="controls" loop="loop" autoplay="autoplay">
  <source src="newdelhi.mp4" type="video/mp4" />
Your browser does not support the video tag.
</video>
</center>


## 4 长周期变化

中国及其周边2012-2020的夜光变化分布图。

[![5bjH7n.jpg](https://z3.ax1x.com/2021/10/28/5bjH7n.jpg)](https://imgtu.com/i/5bjH7n)

从长周期来看，夜光和GDP的发展是有很强的相关性的，可以成为相关分析的一个输入数据源。



## 5 超分辨率

NPP的夜光传感器的实际分辨率是750米，而分发的月度产品在赤道地区的分辨率是500米。目前我们正准备把视觉分辨率从500米提升到250米。

下面是标准的500米尺度的年度变化动画

<center>
<video width="640" controls="controls" loop="loop" autoplay="autoplay">
  <source src="beijing_z1.mp4" type="video/mp4" />
Your browser does not support the video tag.
</video>
</center>

下面是增强到250米尺度的年度变化动画

<center>
<video width="640" controls="controls" loop="loop" autoplay="autoplay">
  <source src="beijing_z2.mp4" type="video/mp4" />
Your browser does not support the video tag.
</video>
</center>

## 6 彩色化

NPP获取的夜光只有强度信息，而SDGSAT1可以获取真彩色的内容。但是NPP的时序从2012开始有持续的价值。我们可以通过将两个数据源的内容融合来获取真彩色的夜光时序。

只融合SDGSAT1的色彩信息

<center>
<video width="640" controls="controls" loop="loop" autoplay="autoplay">
  <source src="npp_color.mp4" type="video/mp4" />
Your browser does not support the video tag.
</video>
</center>

同时融合SDGSAT1的色彩信息和细节纹理信息

<center>
<video width="640" controls="controls" loop="loop" autoplay="autoplay">
  <source src="npp_color2.mp4" type="video/mp4" />
Your browser does not support the video tag.
</video>
</center>

---



**联系方式**

陈甫 副研究员
中国科学院空天信息创新研究院
chenfu@aircas.ac.cn
13811147935

