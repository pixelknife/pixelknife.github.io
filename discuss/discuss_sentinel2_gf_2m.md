# 哨兵二号以及高分系列卫星的大气校正

## 1 欧空局哨兵二号L2A产品

哨兵二号是目前很重要的开源数据资源，但是我之前也已经说到目前的哨兵二号的最新大气校正产品L2A非常蹩脚，是没法用的。

下面是下载的北京周边一个山区的影像

![l1c.jpg](https://s2.loli.net/2022/08/03/L8YaZIpEk291ilV.jpg)
▲ L1C产品（欧空局网站下载）

![l2a.jpg](https://s2.loli.net/2022/08/03/uaPAzKdjJwFZ84m.jpg)
▲ L2A产品（欧空局网站下载）

可以看到L1C产品图像偏蓝（因为有大气成分），而L2A产品整体颜色得到修正，但是山的阴面处理显然不正常，处理后的阴面居然比阳面更亮。

## 2 NASA的HLS产品

目前有个更好的大气校正产品，是NASA做的HLS(Harmonized Landsat and Sentinel-2 surface reflectance data set)

https://hls.gsfc.nasa.gov/

![hs30m.jpg](https://s2.loli.net/2022/08/03/2p6BktRJL4P3cKw.jpg)
▲ HLS.S30产品（EARTHDATA下载）

这个产品使用了处理LANDSAT8/9相同的算法，可以让SENTINLE2和LANDSAT8/9数值上基本一致，混合使用。

但是这个产品把空间分辨率统一缩小到30米，这样的产品失去了原有的10米分辨率，使得应用面大幅缩小。

## 3 像素刻刀HS10M产品

我们使用像素刻刀软件恢复了该产品的空间分辨率到原有的10米，称为HS10M （Harmonized Sentinel2 at 10 Meter）。

![hs20m.jpg](https://s2.loli.net/2022/08/03/KyofB8msPvw29cF.jpg)
▲ HS10M的真彩色组合

而且这个产品是把多个20米红边近红外波段空间分辨率都提升到10米

![hs30m_865.jpg](https://s2.loli.net/2022/08/03/1xKyYg3bXkfsRdr.jpg)
▲ HLS.S30的红边近红外组合（864-781-740）

![hs20m_865.jpg](https://s2.loli.net/2022/08/03/ixlv5c6JGEWYo1U.jpg)
▲ 中间产品，恢复到20米分辨率

![hs10m_865.jpg](https://s2.loli.net/2022/08/03/ziBJYxgq39Vu1p8.jpg)
▲ HS10M产品，恢复到10米分辨率

但是短波红外的B11、B12波段纹理清晰度不到10米（20米插值到10米）。

![hs10m_974.jpg](https://s2.loli.net/2022/08/03/ovTE4FdnK7UlWbL.jpg)
▲ HLS.S30的短波红外-近红外-红边外组合（1612-832-704）

## 4 像素刻刀HG2M产品

国内比较容易获取的数据资源是高分系列、资源系列，很多卫星都有2米分辨率的全色传感器，但是大多数只有4个波段的多光谱。因此高分、资源系列卫星的精确大气校正是比较困难的。

但是如果将国产卫星数据和SENTINEL2以及LANDSAT8/9做融合处理，那么就可以借用S2和L8/9的辐射精度。

![rgb.jpg](https://s2.loli.net/2022/08/03/iqAkVSmyDM9fldj.jpg)
▲ 高分一号可见光2米（和上面的哨兵二号为同一天）

通过像素刻刀软件的处理，将HS10M和它做融合（也需要配准等前置工序）制作了HG2M（Harmonized Gaofen at 2 Meter）。

![gf_321.jpg](https://s2.loli.net/2022/08/03/x7oz3ZIW5wSObK9.jpg)
▲ HG2M产品可见光

更重要的是这样也有了其他波段的信息，是一个2米10波段的数据集，波段中心波谱{ 492, 559, 664, 704, 740, 781, 832, 864, 1612, 2190 }。

![gf_974.jpg](https://s2.loli.net/2022/08/03/rt7RJcPk9musVgh.jpg)
▲ HG2M的短波红外-近红外-红边外组合（1612-832-704）

---

**联系方式**

陈甫 副研究员
中国科学院空天信息创新研究院
chenfu@aircas.ac.cn
13811147935