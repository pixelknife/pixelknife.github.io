# 超分融合提高地物分类精度

## 超分融合

Planet的SuperDove提供3米8波段的数据集，因此可以比较好地用于地物分类。

[![bce7a8.jpg](https://s1.ax1x.com/2022/03/08/bce7a8.jpg)](https://imgtu.com/i/bce7a8)

![pl_3m.jpg](https://s2.loli.net/2022/07/30/WRhxKTYLAIGme6H.jpg)
▲3米尺度，可见光组合(664, 559, 492)

![pl_3m_876.jpg](https://s2.loli.net/2022/07/30/FKUTorEeXM7n8AB.jpg)
▲3米尺度，近红外红边组合(832, 704, 664)

通过超分辨率增强将分辨率提高到2米

![pl_2m.jpg](https://s2.loli.net/2022/07/30/dmJ3N8et6sDb4Fw.jpg)
▲2米尺度，可见光组合(664, 559, 492)

![pl_2m_876.jpg](https://s2.loli.net/2022/07/30/M7gxQySmTl8dXDq.jpg)
▲2米尺度，近红外红边组合(832, 704, 664)

找到相近时间的SENTINEL2，它比SuperDove多了短波红外、近红外等波谱范围的几个波段。

![S2](http://www.geosage.com/highview/figures/Sentinel2_Spectral_Bands.jpg)



![s2_20m_987.jpg](https://s2.loli.net/2022/07/30/6wdebymuC1Jx5hQ.jpg)
▲20米，短波红外近红外组合(2190, 1612, 864)

通过超分融合，可以把两个数据合并成2米13波段的数据集。

![fuse_13bands_131211.jpg](https://s2.loli.net/2022/07/30/2IhAXu8RVQaep7x.jpg)
▲2米尺度，短波红外近红外组合(2190, 1612, 864)

## 分类

更多的波段有助于地物的区分，更高的分辨率有助于细小地物的提取。

![3m.png](https://s2.loli.net/2022/07/30/gIwypU3e9mTFWbK.png)
▲3米8波段分类

![2m.png](https://s2.loli.net/2022/07/30/PaT2Om5wXQgLrcF.png)
▲2米8波段分类

![13band.png](https://s2.loli.net/2022/07/30/bV1Q62kZ3RgWjOD.png)
▲2米13波段分类

我们的实验的体验，面向对象的分类比基于像素的分类更有效，能够解决超分后斑点噪声的问题。

总的来说，2米13波段的数据集提供了更好的分类结果。

---

**联系方式**

陈甫 副研究员
中国科学院空天信息创新研究院
chenfu@aircas.ac.cn
13811147935

