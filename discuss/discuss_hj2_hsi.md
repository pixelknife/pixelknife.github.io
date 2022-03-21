# 环境减灾二号高光谱数据集的高精度处理



环境二号高光谱有可见光近红外VN和短波红外SW两个部分，幅宽96公里，可见光近红外分辨率48米（100波段），短波红外96米（115波段）。

从获取样例看，短波红外存在一些条纹分布噪声，短波红外存在一些点分布噪声。

我们首先通过信号处理削减相关噪声。

▼ 可见光近红外噪声处理前后的动图

[![qmDdlq.gif](https://s1.ax1x.com/2022/03/21/qmDdlq.gif)](https://imgtu.com/i/qmDdlq)

▼ 短波红外噪声处理前后的动图

[![qmDapn.gif](https://s1.ax1x.com/2022/03/21/qmDapn.gif)](https://imgtu.com/i/qmDapn)

我们打算把整个数据集串联起来，形成48米215波段的产品，这样用户用起来更加方便，全谱段的分析成为可能。

因为短波红外分辨率是96米，而且两个传感器相对独立，存在几何成像偏差，因此需要一些精细配准工作。

因为VN的最后一个波段VN100和SW的第一个波段SW001波谱上基本上是一致的，因此可以用他们之间的纹理匹配来调动整个数据集的几何调整。



▼ VN100和SW001之间的位移大概有1~2个像素

[![qmrO54.gif](https://s1.ax1x.com/2022/03/21/qmrO54.gif)](https://imgtu.com/i/qmrO54)

▼ VN100和SW001之间配准完成

[![qmrLaF.gif](https://s1.ax1x.com/2022/03/21/qmrLaF.gif)](https://imgtu.com/i/qmrLaF)


现在就可以把VN和SW按照同样的尺寸和地理信息合并了，变成48米215波段的单个数据集。

[![qmcEiF.jpg](https://s1.ax1x.com/2022/03/21/qmcEiF.jpg)](https://imgtu.com/i/qmcEiF)



样本数据可以在FTP上下载（推荐FTP客户端FTPRUSH）

FTP服务器：  satapp.radi.ac.cn

账号：  cfdata

密码：  cfdata123

目录：  temp/HJ2_HSI/


---

**联系方式**

陈甫 副研究员
中国科学院空天信息创新研究院
chenfu@aircas.ac.cn
13811147935
