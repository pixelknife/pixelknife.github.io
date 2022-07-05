# 欧比特高光谱波段之间配准


欧比特高光谱卫星使用滤光片模式，不同波段的成像时间是不同的。因此在地表存在高程变化的情况下，不同波段之间会存在位移。这样在一些细小纹理的区域可以明显看到波段组合上的红眼皮现象。

这样的问题实质上影响了图像产品的实质分辨率。因为图像上各波段同一个位置像元实质上对应地表不同的位置，这样标称为10米的高光谱可能实际上只能当成20米用，在20米的尺度上才能认为同一像素对应近似同一块地物。

通过像素刻刀软件可以逐个波段修复这样的偏差。

举例说明处理结果

HEM1_20220116234418_0007_L1B_CMOS1

![obt_reg.gif](https://s2.loli.net/2022/07/05/wbIceuzPpgCtQnv.gif)
▲ 动图比较，山区的道路的红颜皮现象最明显

![cmp.png](https://s2.loli.net/2022/07/05/EmLvp4HalC12Z8u.png)
▲ 静态对比

目前这个处理一景（5000x5000x32波段），大概需要60分钟，未来有进一步优化的空间。

下面再通过高光谱数据集的超分辨率，增加分辨率一倍到5米

![cmp3.png](https://s2.loli.net/2022/07/05/12oBGs4fVKkjFht.png)


---

陈甫 副研究员
中国科学院空天信息创新研究院
chenfu@aircas.ac.cn
13811147935
