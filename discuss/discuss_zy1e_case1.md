# ZY1E高光谱超分辨率增强处理案例

ZY1E的高光谱数据由可见光近红外VN、短波红外SW两个传感器组成，其中VN有76个波段，SW有90个波段。但是这两个传感器之间有一定的几何偏差。通过精细配准可以将两个传感器合在一起，成为166个波段的高光谱。

下图是像素刻刀软件(PixelKnife)推算的位移偏差图，其中最亮的地方为0.5像素位移。



[![bjGsgA.jpg](https://s1.ax1x.com/2022/03/15/bjGsgA.jpg)](https://imgtu.com/i/bjGsgA)



然后使用超分辨率增强技术提高2倍分辨率，从30米分辨率的数据集变成15米。提升效果如下图所示。

▼ 30米的高光谱立方体

[![bjaxPK.jpg](https://s1.ax1x.com/2022/03/15/bjaxPK.jpg)](https://imgtu.com/i/bjaxPK)

▼ 15米的高光谱立方体

[![bjaz8O.jpg](https://s1.ax1x.com/2022/03/15/bjaz8O.jpg)](https://imgtu.com/i/bjaz8O)

▼ 可见光组合（32-20-12）的比较

[![bjNzo6.md.jpg](https://s1.ax1x.com/2022/03/15/bjNzo6.md.jpg)](https://imgtu.com/i/bjNzo6)



可以看到这里的田地、道路、建筑等细小纹理明显增加了，更符合实际情况。

这些新的纹理信息是完全从本数据集内在挖掘而来，算法的实质是将高光谱数据集中丰富的波谱信息部分体现到空间分辨率上，这对于大多数高光谱数据集都有明显的效用。

样本数据可以在FTP上下载（推荐FTP客户端FTPRUSH）

FTP服务器：  satapp.radi.ac.cn

账号：  cfdata

密码：  cfdata123

目录：  temp/zy1e/

其中的文件说明：

ZY1E_AHSI_E125.34_N45.89_20210420_008407_L1A0000333282.ZIP 原数据集

30M.TIF 几何精校正后，将VN和SW合并成166波段的高光谱数据集

15M.TIF 通过超分辨率增强技术，将分辨率提升到15米

---

陈甫 副研究员
中国科学院空天信息创新研究院
chenfu@aircas.ac.cn
13811147935