# ZY1E的高光谱处理（VN篇）

ZY1E上有一个30米高光谱，其中可见光近红外(VN)76波段，短波红外(SW)90波段。其中VN数据信噪比较好，我们尝试将其空间分辨率提高3倍到10米。



[![oZei6J.jpg](https://z3.ax1x.com/2021/11/26/oZei6J.jpg)](https://imgtu.com/i/oZei6J)



从增强后的10米图像中可以明显地看出来，原来的30米图像中的每个像素的卷积核不是正常的矩形（或者说圆型），而是纵向长的矩形（或者说椭圆形）。这个可能是成像的积分时间或者其他因素没有控制好的结果。这个原则上应该通过预处理前期消除掉。



每个波段处理前后的对比：

▼ 1-20
[![oZuFXQ.jpg](https://z3.ax1x.com/2021/11/26/oZuFXQ.jpg)](https://imgtu.com/i/oZuFXQ)

▼ 21-40
[![oZuM1U.jpg](https://z3.ax1x.com/2021/11/26/oZuM1U.jpg)](https://imgtu.com/i/oZuM1U)

▼ 41-60
[![oZu3nJ.jpg](https://z3.ax1x.com/2021/11/26/oZu3nJ.jpg)](https://imgtu.com/i/oZu3nJ)

▼ 61-76
[![oZuG7R.jpg](https://z3.ax1x.com/2021/11/26/oZuG7R.jpg)](https://imgtu.com/i/oZuG7R)

---

**联系方式**

陈甫 副研究员
中国科学院空天信息创新研究院
chenfu@aircas.ac.cn
13811147935
