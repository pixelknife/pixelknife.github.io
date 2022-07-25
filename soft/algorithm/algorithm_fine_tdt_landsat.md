# 高分卫星正射产品的几何精校正+辐射精校正

国产系列卫星中的2米尺度卫星很多，我们制作了大量的“正射产品”。因为卫星参数不够精确，所使用的DEM精度也有限，这些产品并不是严格正射的，不同时相产品之间存在几何偏差，特别是在山地地形起伏的地区。而且因为多个卫星多个传感器的特性不同，因此做图的色彩有差异。

将之前制作的不同年份的图叠放到一起

![old2.gif](https://s2.loli.net/2022/07/23/IBpLw3NMKqVy1tF.gif)

可以看到有明显的几何的偏离和颜色的差异，注意力难以集中到小的地表实质性变化。



像素刻刀软件通过天地图的底图作为参考对这些数据做几何精校正，用landsat全国无云影像作为参考做辐射精校正。

![new.gif](https://s2.loli.net/2022/07/23/Fwy47WhvKg5Ja9u.gif)

可以看到新产品保持了几何和辐射的稳定。山体没有明显的位移，图像颜色更加准确鲜艳，减少了高饱和的区域。



使用这样的产品，用户可以将注意力集中到地物实质性变化的内容上。这项技术在多期图像的变化检测中可以发挥重要的作用。



---

**联系方式**

陈甫 副研究员
中国科学院空天信息创新研究院
chenfu@aircas.ac.cn
13811147935