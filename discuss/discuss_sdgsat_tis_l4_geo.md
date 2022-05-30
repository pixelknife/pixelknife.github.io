# SDGSAT-TIS的L4产品的内部几何形变

TIS传感器采用摆扫方式，相对于推扫方式有更多的内在几何形变的变量因素。比如摆镜的速度是否均匀，正向和反向扫之间的差异等等。

总的来说目前的TIS的L4产品存在内部形变，这在多时相变化检测上是一个挑战。

比如4月8日和5月4日的上海虹桥机场周边的图像动图如下

[![Xl60xS.gif](https://s1.ax1x.com/2022/05/30/Xl60xS.gif)](https://imgtu.com/i/Xl60xS)

直接对比还有很明显的几何偏移

通过像素刻刀PixelKnife的非线性几何配准，可以将两者改正到0.1像元偏差以下。

[![Xl6DKg.gif](https://s1.ax1x.com/2022/05/30/Xl6DKg.gif)](https://imgtu.com/i/Xl6DKg)

看一下调整前后的位移情况

[![Xl6rrQ.gif](https://s1.ax1x.com/2022/05/30/Xl6rrQ.gif)](https://imgtu.com/i/Xl6rrQ)





---

**联系方式**

陈甫 副研究员
中国科学院空天信息创新研究院
chenfu@aircas.ac.cn
13811147935

