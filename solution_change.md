# 逐日地表自动变化监测

PlanetScope小卫星群是用于地表变化监测的最重要的数据源，它有一百多颗卫星，分辨率达到3.3米，具备了每天覆盖地球一次以上的能力。

但是因为是廉价小卫星，因此在几何、辐射等方面都不能和造价昂贵的大卫星相比。但是如果在处理软件上多下点功夫，还是可以起到物尽其用的效果。



以最近的新闻焦点阿富汗喀布尔机场为例，描述一些处理的基本步骤。



1）8月14日和8月15日的分发数据的图像内容表现如下

[![f48kzd.gif](https://z3.ax1x.com/2021/08/17/f48kzd.gif)](https://imgtu.com/i/f48kzd)



2）以8月15图像为基准，调整8月14日的影像，实现精细化配准

[![f48FRH.gif](https://z3.ax1x.com/2021/08/17/f48FRH.gif)](https://imgtu.com/i/f48FRH)



3）配准后的两个时相

[![f48EQA.gif](https://z3.ax1x.com/2021/08/17/f48EQA.gif)](https://imgtu.com/i/f48EQA)



4）图像增强以及锐化，突出纹理细节

[![f48ZLt.gif](https://z3.ax1x.com/2021/08/17/f48ZLt.gif)](https://imgtu.com/i/f48ZLt)



5）去除非实质性的低频变化，保留高频变化部分


[![f48VsI.gif](https://z3.ax1x.com/2021/08/17/f48VsI.gif)](https://imgtu.com/i/f48VsI)



6）制作变化幅度图

[![f4JTdP.jpg](https://z3.ax1x.com/2021/08/17/f4JTdP.jpg)](https://imgtu.com/i/f4JTdP)



因为两日的成像时间相差一个小时，所以太阳的高度角不同。8月15日不少民房因为和太阳光角度成镜面反射，因此在图像上形成了较多的高亮度的白斑，而在8月14日的影像上较少。这个也是光学遥感的一个固有问题。



---



**联系方式**

陈甫 副研究员
中国科学院空天信息创新研究院
chenfu@aircas.ac.cn
13811147935

