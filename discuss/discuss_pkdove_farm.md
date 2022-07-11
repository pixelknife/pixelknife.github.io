# pkDove的农林应用


[![bce7a8.jpg](https://s1.ax1x.com/2022/03/08/bce7a8.jpg)](https://imgtu.com/i/bce7a8)
▲ SuperDove、Sentinel2的波谱关系

SuperDove相对于Sentinel2有更高的空间分辨率，更适合中国较小的农地。相对于相近空间分辨率的国产高分卫星（GF1A/B/C/D、GF6 )，它有对植被辨识很重要的红边波段。

pkDove是通过像素刻刀（PixelKnife）软件对Planet的SuperDove卫星数据做的质量提升，将3米8波段的分发产品，提高到2米8波段，而且其波谱数值可以用于定量化分析。

我们用pkDove处理了黑龙江哈尔滨附近的SuperDove数据样例

![cmp_642.jpg](https://s2.loli.net/2022/07/11/vJlSM9bPN7mVnDL.jpg)
▲ 可见光自然色组合（6-4-2），处理前后比较

![cmp_876.jpg](https://s2.loli.net/2022/07/11/lI2tp3Ez7TAqjW6.jpg)
▲ 近红外红边组合（8-7-6），处理前后比较

可以看到看到不同地块中叶绿素表现差异，从近红外、红边上最为明显。



---



陈甫 副研究员
中国科学院空天信息创新研究院
chenfu@aircas.ac.cn
13811147935