# 天下无云

光学遥感的首要难题就是会受到云雾等大气现象的干扰，难以保证图像质量。我们通过算法合成无云的密集影像时序产品“天下无云”，让遥感分析变得非常简单、所见即所得，不需要专业训练或者专业工具就可以做出分析判断，形成傻瓜化的遥感应用。

## 1 中分辨率

这些卫星的时间覆盖率较高，可以通过综合多期数据来完成无云产品。

我们制作了天下无云的旬产品（10天间隔），2020年36帧北京时序。

可以通过下面的WEBGIS来访问：

[![5bR7P1.jpg](https://z3.ax1x.com/2021/10/28/5bR7P1.jpg)](https://imgtu.com/i/5bR7P1)

[![5bRH8x.jpg](https://z3.ax1x.com/2021/10/28/5bRH8x.jpg)](https://imgtu.com/i/5bRH8x)

[http://satsee.radi.ac.cn/cfdata/cloudless/beijing/](http://satsee.radi.ac.cn/cfdata/cloudless/beijing/)

如果觉得响应慢，可以简化成12帧的月度时序，这样只要加载1/3的图像数据。

[http://satsee.radi.ac.cn/cfdata/cloudless/beijing/index12.html](http://satsee.radi.ac.cn/cfdata/cloudless/beijing/index12.html)

## 2 高分辨率

这些卫星数据的获取成本较高，通常不会有太高的冗余，而且时相可能分布很广，涉及不同的季节。

我们先通过中分辨率卫星制作一张参考无云影像，然后再此基础上，将高分辨率卫星影像映射或者仿真成参考影像的色调，使得整个数据集高度统一，可视效果好。

[![5qkWQI.jpg](https://z3.ax1x.com/2021/10/28/5qkWQI.jpg)](https://imgtu.com/i/5qkWQI)

可以浏览以下案例来体会一下

[广东2米2021年版](http://satsee.radi.ac.cn:8080/guang/guang.html?uid=8e0848ab-8540-4206-90c3-29a5c2752c91)

[黑龙江2米2021年版](http://satsee.radi.ac.cn:8080/guang/guang.html?uid=47bc4e36-feff-4a0c-b03a-b0aa55a07864)

---



**联系方式**

陈甫 副研究员
中国科学院空天信息创新研究院
chenfu@aircas.ac.cn
13811147935