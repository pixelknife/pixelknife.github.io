# 目前最精细的中国太阳能潜力分布数据集“葵花” (SunFlower)



论文链接

[Estimation of Photovoltaic Energy in China Based on Global Land High-Resolution Cloud Climatology](https://www.mdpi.com/2072-4292/14/9/2084/htm)



## 研究背景

光资源作为一种可再生的清洁能源，光伏发电可以减少传统能源发电造成的臭氧层损耗和气候恶化状况。光伏电站位置的选择对发电成本有着直接影响，决定了光能的产出。因此光伏发电站的选址在能源战略中具有重要地位。传统的光资源分布估算主要依赖于气象站点的太阳辐射数据或者其他气候要素（其中最常用是日照百分率）对太阳辐射的反演。但气象站空间的连续性差，而且分布没有规律，没有考虑气象要素自身的分布特性，误差较大。采用卫星遥感观测的云量数据估算日照百分率，进而估算光资源分布能解决这一问题。

本研究使用1km的中国区域的旬云频率产品GLHCC，按照Rangarajan的模型集成日照百分率的基础数据。利用中国区域的72个气象站点的日照时长数据和太阳辐射数据分季度进行线性和非线性拟合，得到了每个站点的各个模型的季节最佳拟合参数。通过对各个模型的拟合结果的误差检验，选出了最适用中国区域的光资源预测模型Sen模型。将利用云量集成的每旬日照百分率和季度参数代入到最佳模型，结合地形遮挡，估算中国区域的光资源分布。

最后通过与世界银行的发电潜力数据和国家太阳辐射的辐照度进行对比，证明了本研究的中国区域的光资源分布分数能够较为准确的反映中国区域的光资源分布，能够为光伏发电站的选址提供重要参考。

## 产品比较

本研究中使用到的对比数据是世界银行的发电潜力数据和光伏地理信息系统的辐照度数据。

世界银行已发表的研究报告提供了太阳能资源的聚合和统一视图，并从国家和地区来看公用事业规模光伏电站的发展潜力。

光伏地理信息系统的太阳辐射数据是根据国家可再生能源实验室开发的国家太阳辐射数据库 (NSRDB) 计算得出的。NSRDB 连续完整地收集了三种最常见的太阳辐射测量值（全球水平、直接法向和漫射水平辐照度）和气象数据的每小时和每半小时值。提供的数据是长期平均值，根据 2005 年至 2015 年期间的每小时全球和漫射辐照度值计算得出，空间分辨率是5公里。

为了验证本研究中中国区域的光资源分布分数的准确性，选取了世界银行的太阳能发电潜力数据与国家太阳辐射数据库的年度太阳辐射数据进行视觉对比。

[![7QFw60.png](https://s4.ax1x.com/2022/01/13/7QFw60.png)](https://imgtu.com/i/7QFw60)
▲葵花产品的年度光资源分布分数图

[![7QFdlq.png](https://s4.ax1x.com/2022/01/13/7QFdlq.png)](https://imgtu.com/i/7QFdlq)
▲世界银行的太阳能发电潜力

[![7QFapn.png](https://s4.ax1x.com/2022/01/13/7QFapn.png)](https://imgtu.com/i/7QFapn)
▲国家太阳辐射数据库的2005~2015年的水平面上的年平均辐照度

由于国家太阳辐射数据的太阳辐射数据只包括非洲、部分欧洲、部分亚洲、部分南美洲以及部分澳洲的区域，因此中国区域的太阳辐射并不完整。

三种产品整体上的光资源分布大致相同，中国的青藏高原区域和柴达木盆地的光资源分布最为丰富，四川盆地地区的光资源最为稀缺。呈现这样形式的光资源分布的主要原因是青藏高原海拔高，空气比较稀薄，水汽含量少，云量较少，对太阳辐射的削弱作用小，到达地面的太阳辐射强；另外，青藏高原纬度较低，终年正午太阳高度平均较大，太阳辐射强。而柴达木盆地地处西北荒漠化地区深居内陆，属于干旱、半干旱地区，降水少，日照时间长，且处于中国第一梯度地区，海拔高，大气对太阳辐射的削弱作用小。而四川盆地水汽不易散发，空气中水汽含量多，阴天、雾天较多，从而造成日照的时间短，日照强度弱，太阳能资源贫乏。

但从细节上讲，三者还存在许多不同之处，尤其是世界银行的发电潜力图，与本研究的光资源分布分数以及国家太阳辐射数据库的太阳辐射数据有较大差异。世界银行的发电潜力在中国的不同分区上存在着明显的差异和边界，比如新疆塔里木盆地和准噶尔盆地的发电潜力与周围发电潜力相比明显较小，且东北区域也存在明显分界线。华东、华南、华中地区与其他地区的差异也比其他两个产品的差异大。这可能与中国不同分区间采用的模型参数不同有关。而本研究的产品与国家太阳辐射数据库的数据的不同主要体现在准噶尔盆地，本研究的年度产品在天山以南地区没有体现出与周围区域明显的差别。

除此上述明显区别外，在一些小的区域，世界银行的发电潜力与本研究的光资源分布以及国家数据库的辐照度呈现出了完全相反的结果，尤其是地势崎岖较大的山区。四川省金川县有着独特的气候条件,日照时间长，年平均日照小时数超过2400小时，有“高原阳光城”的美誉，是典型的河谷县。因此以金川县为例，展示三个产品在该地区的光资源分布结果并分析金川县的光资源利用情况（图4.12）。

[![7Q9pKU.png](https://s4.ax1x.com/2022/01/13/7Q9pKU.png)](https://imgtu.com/i/7Q9pKU)
▲从上到下、从左到右分别是金川县90m分辨率的数字高程模型、葵花、世界银行、国家太阳辐射数据库。

从图中可以发现，本研究的光资源分布分数与国家太阳辐射数据库的辐照度表现相似，在河谷区域呈现了较丰富的光资源，在山坡上则呈现了较稀缺的光资源分布。而世界银行发布的该地区的发电潜力却与本研究的光资源以及国家太阳辐射数据库的辐照度相反，发电潜力与海拔高度存在某种正相关的关系，海拔越低，发电潜力越低，海拔越高，发电潜力越高。经过调查发现，本研究的光资源分布与国家太阳辐射数据库的辐照度更符合事实情况。因为该地区的河谷是典型的干热河谷。干热河谷是指高温、低湿河谷地带，在地理学上是一种小尺度范围的自然景观。我国干热河谷主要分布于金沙江、元江、怒江、南盘江等沿江的四川攀枝花、云南和贵州等地区。区域内光热资源丰富，气候炎热少雨。按理河谷本应是最不缺水的地方，可好多的峡谷河畔却荒凉一片。干热河谷的成因，最主要的影响因素被归结为：“焚风效应”和“山谷风局地环流效应”。焚风效应是指焚风过境的时候会使该区域的气候变得火热和干燥。焚风是气流越过高山后下沉造成的，每下降1000米，温度升高10摄氏度左右。而山谷风是出现于山地及其周边地区的，具有日周期的地方性风。白天，山坡接受太阳光热较多，空气增温较多；而与山顶相同高度的山谷上空，因离地较远，空气增温较少。由于山坡上的暖空气不断膨胀上升，在山顶的近地面形成低压，并在山谷的上空从山坡流向谷地上空积聚，谷地上空空气受重力影响收缩下沉，在谷底近地面形成高压，下沉气流形成干热的环境。在干热河谷，经常可看到两侧山腰有一条云带，这其实是谷风气流上升而形成的。在干热河谷地带应该是河谷的光资源高于山坡的光资源。因此本研究的光资源分布与国家太阳辐射数据库的辐照度更符合事实情况。世界银行的发电潜力呈现的相反的结果或许是过多的考虑了地形引起的光资源的变化，而较为忽视了云量的影响，因此，使用云量来估算光资源分布非常有现实意义。

**经过上面的比较，可以看出葵花相对于目前市面上的产品有明显的优势，相对于世界银行的产品更符合事实，相对于国家太阳辐射数据库更加完整、空间分辨率更高。对于太阳能电站建设，具有更好的工程应用价值。**

---



**联系方式**

陈甫 副研究员
中国科学院空天信息创新研究院
chenfu@aircas.ac.cn
13811147935