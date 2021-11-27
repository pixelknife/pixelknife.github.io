# ZY1E高光谱VN和SW的配准

ZY1E的高光谱是有可见光近红外(VN)和短波红外(SW)两个部分组成的，因为硬件的局限性，这两个之间有很严重的非线性几何误差。

▼ 我们用VN的76波段和SW的1波段之间做个动图比较

[![oeejyQ.gif](https://z3.ax1x.com/2021/11/27/oeejyQ.gif)](https://imgtu.com/i/oeejyQ)

可以看到这里明显的非线性内部偏移，这用普通遥感软件是处理不了的。

我们的像素刻刀(PixelKnife)可以非常精确的修复这样的偏差。

▼ 以VN76不动，SW01去靠拢

[![oeeOSS.gif](https://z3.ax1x.com/2021/11/27/oeeOSS.gif)](https://imgtu.com/i/oeeOSS)

▼ 再看一下SW01需要做的位移的情况

[![oeeXQg.gif](https://z3.ax1x.com/2021/11/27/oeeXQg.gif)](https://imgtu.com/i/oeeXQg)


现在几何偏差已经可以修复得非常准确。但是可以看到这里还有亮度上得偏差，原则上VN76和SW01波谱上非常接近，图像内容应该很像才对。

---

**联系方式**

陈甫 副研究员
中国科学院空天信息创新研究院
chenfu@aircas.ac.cn
13811147935

