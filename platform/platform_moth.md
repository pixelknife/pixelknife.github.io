# “飞蛾”高分辨率近实时精准火点卫星监测系统投入实用

---

相比于俄罗斯、美国、巴西、澳大利亚等森林大国的佛系灭火策略，中国对森林火灾的重视程度是最高的，但是积极主动灭火也时常遭受人员损失。

[![hCQ35V.jpg](https://z3.ax1x.com/2021/08/23/hCQ35V.jpg)](https://imgtu.com/i/hCQ35V)

美国2018年CAMP大火的发展过程

通过卫星开展对林火状态的及时精准的监测是非常重要的。这里有几个要素：时间延迟要小（长了就没有实用性了），空间分辨率要高（这样才能发现小火），准确度要高（遗漏或者误判都会带来损失）。

目前国内实用的林火监测系统主要依赖日本的葵花卫星8号，它是一颗地球同步轨道气象卫星，可以10分钟对日本为中心的半球成像一次（中国中东部包含在内）。它的优点是除了拍摄频率高达10分钟以外，系统处理的延迟也比较少，大概在20～30分钟。它的缺点是分辨率较粗，大概在2000米尺度。此外美国的EOS、NPP、NOAA20等极轨气象卫星也是重要的数据源，他们的分辨率在500～1000米，每颗星一天大概白天黑夜各访问一次。

要想真正的使用卫星开展火点实时监测任务，需要几个条件：首先要能够自主接收或者快速接入卫星下行数据，第二要能够快速解码成像，第三要能够准确定位火点信息。

中国遥感卫星地面站主要是接收分辨率较高的陆地观测卫星。**只要该卫星具备短波红外、中红外等对高温敏感的波段就可以用于火点监测**。我们之前已经使用Landsat8、Sentinel2、GF4等卫星的产品数据用于林火监测。但是火点产品是在卫星正式分发产品的基础上开展的，这样对于追求时效性还未能达到理想的程度。

![hCQlEq.jpg](https://z3.ax1x.com/2021/08/23/hCQlEq.jpg)



Landsat7/8卫星的波段分布

因为地面站能够直接接驳Landsat8卫星，而且完全掌握其数据码流特性，所以有条件更进一步。新一代的基于Landsat8下行数据的近实时火点产品数据推出了。不需要将数据转换成标准景，我们直接在整轨卫星下行数据上检测火点，大大提高了火点检测的速度。单轨下行数据火点产品的生产时间在15分钟以内，火点敏感波段分辨率30米，火点定位误差<50m。



![hCQMbn.png](https://z3.ax1x.com/2021/08/23/hCQMbn.png)



目前近实时火点的延时主要是接收站向北京本部的数据传输时间。卫星数据从接收站传输到地面站本部的时间随数据传输任务的多少有所波动，一轨数据的传输时间大多在30分钟以内。所以Landsat8近实时火点的实际延时在45分钟以内。以后随着数据传输性能的提高，火点产品的时效性会进一步加强。

热红外数据受空间分辨率往往较低，以及大气背景等方面影响，对小面积温度目标反演提取精度较低。而经过大量研究表明采用短波红外波段进行温度反演则有更高的敏感性，利于小面积高温目标的反演。例如农田秸秆燃烧和工矿企业的排放，单个燃烧区域规模小，分布零散。用短波红外能很精准的检测出异常高温目标。

[![hCQ1U0.png](https://z3.ax1x.com/2021/08/23/hCQ1U0.png)](https://imgtu.com/i/hCQ1U0)

国家电网测试发现Landsat8比NPP产品精度高得多

因此这套“飞蛾”(Moth)火点监测系统具有高分辨率(30米)、近实时(<45分钟)、精准(短波红外)的重要特性。

近期本系统成功中标“**国网输电线路山火资源卫星火情识别及数据更新服务**” 项目，以近实时火点产品补充山火卫星火情数据库中的火点产品源，服务于中国国家电网的线路安全监测工作。

后续我们将持续开发近实时火点产品的数据源，通过增加HJ2A/2B、Landsat9、广目卫星等具备高分辨率火点监测能力的卫星资源，提高近实时火点产品的时间分辨率。

---


**联系方式**

陈甫 副研究员
中国科学院空天信息创新研究院
chenfu@aircas.ac.cn
13811147935