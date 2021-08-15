# 高精度配准



处理高分卫星数据时首先要处理可见光RGB波段之间的偏差、多光谱和全色之间的偏差。

以一景GF2为例

分发的数据集中全色和多光谱之间，右半边不动，左半边有明显偏差
[![f264yD.gif](https://z3.ax1x.com/2021/08/15/f264yD.gif)](https://imgtu.com/i/f264yD)

如果不配准直接融合，会导致严重的模糊和失真
[![f265Oe.gif](https://z3.ax1x.com/2021/08/15/f265Oe.gif)](https://imgtu.com/i/f265Oe)

基于梯度场的非线性几何配准后，误差应该低于0.1像元
[![f26hQO.gif](https://z3.ax1x.com/2021/08/15/f26hQO.gif)](https://imgtu.com/i/f26hQO)

调整前后的多光谱的位移
[![f26oeH.gif](https://z3.ax1x.com/2021/08/15/f26oeH.gif)](https://imgtu.com/i/f26oeH)



---

**联系方式**

陈甫 副研究员
中国科学院空天信息创新研究院
chenfu@aircas.ac.cn
13811147935

