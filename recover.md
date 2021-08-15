# 不失真融合



高分辨率卫星通常采用高空间分辨率的全色和低空间分辨率的多光谱的组合，分辨率上大多数是4倍的关系。需要通过融合算法形成高分辨率多光谱的产品图像。

常用的商业遥感软件的融合算法往往有较大的颜色偏差，导致后续定量化的算法难以开展。



下面利用WorldView3的0.3/1.2米样本数据做了能够做定量化测试的数据集，右边是缩小1/4退化成1.2米/4.8米的输入数据集，左边是1.2米的原始多光谱作为真值来测试算法的误差。

[![f2UZ9J.png](https://z3.ax1x.com/2021/08/15/f2UZ9J.png)](https://imgtu.com/i/f2UZ9J)

下面比较了ENVI的GS、NND、PCI的pansharp以及像素刻刀(pk)的差异。

[![f2YfHO.gif](https://z3.ax1x.com/2021/08/15/f2YfHO.gif)](https://imgtu.com/i/f2YfHO)

[![f2YWDK.gif](https://z3.ax1x.com/2021/08/15/f2YWDK.gif)](https://imgtu.com/i/f2YWDK)

[![f2Ygjx.gif](https://z3.ax1x.com/2021/08/15/f2Ygjx.gif)](https://imgtu.com/i/f2Ygjx)

[![f2YRu6.gif](https://z3.ax1x.com/2021/08/15/f2YRu6.gif)](https://imgtu.com/i/f2YRu6)

实际应用PixelKnife处理GF2，融合前后的多光谱的波谱差异很小。
[![f26Twd.gif](https://z3.ax1x.com/2021/08/15/f26Twd.gif)](https://imgtu.com/i/f26Twd)





---

**联系方式**

陈甫 副研究员
中国科学院空天信息创新研究院
chenfu@aircas.ac.cn
13811147935

