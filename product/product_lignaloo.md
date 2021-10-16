# 云分布统计产品



我们小组在学术期刊Remote Sensing上发表了一篇文章
[Global Land High-Resolution Cloud Climatology Based on an Improved MOD09 Cloud Mask](https://www.mdpi.com/2072-4292/13/19/3997/htm)
描述了我们制作的10天1公里分辨率的全球云气候产品。



**摘要**

云在地球-大气系统的能量和水分循环中起着重要作用，影响着自然界和人类社会的许多重要过程。然而，可用于高分辨率模式的细粒度和高精度全球云气候学数据非常少。在本文中，我们根据2001年至2016年的MOD09云罩产品制作了一份10天1公里分辨率的全球陆地云气候学（GLHCC）产品。对原始MOD09云遮罩的两项改进（短波红外和波段2/6比值阈值法）减少了被错误归类为云的雪、冰和明亮区域。初步云产品通过变分静止噪声去除器（VSNR）去除轨道伪影，并去除异常反照率区域，以生成最终云气候学数据。从3777个全球气象站收集的地面云观测直接验证了新产品。来自高级甚高分辨率辐射计（AVHRR）和MOD/MYD35的PATMOS-X作为GLHCC一致性检查的对比产品。评估结果表明，GLHCC显示出与地面站观测值、MOD/MYD35和PATMOS-X的强相关性。当地面观测值作为真值时，GLHCC和MOD/MYD35显示出比PATMOS-X更高的精度。在大多数选定的感兴趣区域，三者表现不同，GLHCC比MOD/MYD35和PATMOS-X更符合事实。GLHCC可以很好地代表过去16年的云分布，并将在自然和人类社会许多方面的细粒度需求中发挥重要作用。

![](https://www.mdpi.com/remotesensing/remotesensing-13-03997/article_deploy/html/images/remotesensing-13-03997-g001-550.jpg)



**数据集**

数据按照日期分割成36期，每个月3期，每个月最后一期包含的日期不一定为10。（这个和论文中不同）

这样也可以方便把连续3期合并成月度产品，也可以把连续9期合并成季度产品。

每期图像是一个8位的压缩TIF图像，0~100是有效数值，255是NODATA。每期图像大概500MB，数据集总量为18GB。

存放在百度网盘上提供长期下载：

链接：[https://pan.baidu.com/s/13d3qNB7BJAcBieobbv_CcQ ](https://pan.baidu.com/s/13d3qNB7BJAcBieobbv_CcQ)
提取码：65qi



**动态访问**

通过动态WEBGIS可以访问该数据集

[http://satsee.radi.ac.cn/cfdata/doc/cloudmap/](http://satsee.radi.ac.cn/cfdata/doc/cloudmap/)



---



**联系方式**

陈甫 副研究员
中国科学院空天信息创新研究院
chenfu@aircas.ac.cn
13811147935

