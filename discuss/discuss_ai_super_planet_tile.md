#  AI超分辨率(Planet网站瓦块3米到1米)

Planet公司发射了一百多颗Planetscope卫星，形成了接近全球每日访问的遥感数据获取。在此基础上，Planet网站制作了月度（无云）产品，对于中国多云雨地区还是很有价值的。美中不足的是Planetscope卫星的分辨率是3米，地物纹理不甚清楚。

我们收集Planetscope数据与GF2形成训练集，通过AI模型形成业务化流程。输入Planet网站上的瓦块数据（3米），输出模仿对应高分二号的图像（1米）。

下面是我们在广西一个项目中的实际案例。这个项目的核心是要在广西这个多云雨的地方实现月度以上频率的卫星数据覆盖，我们使用了2~3米的数据源并加以超分来实现用户的需求。

![3b041b2a33b6818eb5adae253566918.png](https://s2.loli.net/2023/12/23/GlMWVgrAtUyjoEZ.png)

![848c2dd2da585a407608465db9b40e2.png](https://s2.loli.net/2023/12/23/9FJvEUbfH7u1CnQ.png)



Planet网站瓦片数据的超分前后比较实例

![1.gif](https://s2.loli.net/2023/12/22/7s3IYuBHlpOhjSE.gif)

![2.gif](https://s2.loli.net/2023/12/22/65AIiVmrvDLRCY1.gif)

![3.gif](https://s2.loli.net/2023/12/22/NTMj1AGUkaS2b5J.gif)

![4.gif](https://s2.loli.net/2023/12/22/zMWgrSIRqVhm5wD.gif)

![5.gif](https://s2.loli.net/2023/12/22/LFYJK6NqmTREvXU.gif)


通过我们的像素刻刀(PixelKnife)软件可以得到目前世界高水准的视觉体验，充分发挥卫星影像的信息潜力。


---

**联系方式**

陈甫 副研究员
中国科学院空天信息创新研究院
chenfu@aircas.ac.cn
13811147935