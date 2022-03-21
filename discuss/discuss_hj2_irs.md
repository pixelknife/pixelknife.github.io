# 环境减灾二号红外传感器的高精度处理



红外传感器有5个48米分辨率（VN近红外、短波红）的和4个96米分辨率的（IRS中红外到远红外）。但是可能和它的横向扫描成像方式有关，拿到产品图像的几何畸变还是比较明显的。

这里先对图像内部的波段之间的错位做一些分析和修复。

▼ IRS波段1/2之间比较，可以感受到明显的位移

[![qnGiRS.gif](https://s1.ax1x.com/2022/03/21/qnGiRS.gif)](https://imgtu.com/i/qnGiRS)

▼ 像素刻刀软件追踪的位移强度图

[![qnGSat.jpg](https://s1.ax1x.com/2022/03/21/qnGSat.jpg)](https://imgtu.com/i/qnGSat)

▼ 将波段1做相对位移调整

[![qnGCPf.gif](https://s1.ax1x.com/2022/03/21/qnGCPf.gif)](https://imgtu.com/i/qnGCPf)

▼调整后的波段1和波段2之间已经是对齐了

[![qnGPG8.gif](https://s1.ax1x.com/2022/03/21/qnGPG8.gif)](https://imgtu.com/i/qnGPG8)

▼在更大的范围看，可以发现一种横向扫描的痕迹

[![qnGpIP.jpg](https://s1.ax1x.com/2022/03/21/qnGpIP.jpg)](https://imgtu.com/i/qnGpIP)

此外两个相邻扫描行之间的几何错位也需要后续考虑，东西两侧可以看到较大的错位偏差。

---

**联系方式**

陈甫 副研究员
中国科学院空天信息创新研究院
chenfu@aircas.ac.cn
13811147935
