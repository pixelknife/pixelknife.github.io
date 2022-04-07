# pkDove案例集锦

pkDove是通过像素刻刀（PixelKnife）软件对Planet的SuperDove卫星数据做的质量提升，将3米8波段的分发产品，提高到2米8波段，而且其波谱数值可以用于定量化分析。

这里的超分辨率技术是核心关键，这在之前已经做过[介绍](discuss_superdove_x2.html)。但是我们目前还是把超分的目标定在2米而不是1.5米。这有以下几点考虑：1）3米分辨率也不是实际成像分辨率而是制图分辨率，其公布的实际成像分辨率应该是接近4米；2）2米是我国高分系列等多数光学卫星常用的分辨率，而1.5米则几乎没有，如果联合制图实际上还需要返回2米；3）2米输出文件相对来说文件大小不会增加太多，信息量也是充分的。

[![bce7a8.jpg](https://s1.ax1x.com/2022/03/08/bce7a8.jpg)](https://imgtu.com/i/bce7a8)

我们发现SuperDove对Sentinel2做了波谱映射仿真但是并不彻底，因为其中1、3、5三个波段因为在Sentinel2中没有对应波段（10/20米对应），所以应该是没有处理的，而pkDove中则根据他们和相近可见光波段的相关性也做了对应调整，使得整个波谱在数值上连续稳定，这样后续可做一些波谱上的数值分析也是可以的了。

[![q4JMFJ.jpg](https://s1.ax1x.com/2022/04/01/q4JMFJ.jpg)](https://imgtu.com/i/q4JMFJ)

上图左边是Planet分发的产品，其中1、3、5波段和2、4、6波段形成锯齿状的起伏，这是很不正常的，右侧是pkDove处理后的，不仅图像分辨率增强了，而且波谱数值也正常了。

我们用pkDove处理了一系列的Planet分发的整景数据产品来检验产品。因为Planet星座是由100多颗卫星组成的，所以各个卫星的成像质量差异还是比较大的，图像的模糊（散焦）程度也不同，因此我们会对整景图像的中间部分做一个测试来确定选择强弱两级超分参数（命令行中锐化参数5或者6）来处理图像，通常使用更强参数的处理结果图像上噪声可能就会更明显一些。



[![LSwwdI.jpg](https://s1.ax1x.com/2022/04/07/LSwwdI.jpg)](https://imgtu.com/i/LSwwdI)
▲ 美国加州圣迭戈海军基地

[![LSw6SS.jpg](https://s1.ax1x.com/2022/04/07/LSw6SS.jpg)](https://imgtu.com/i/LSw6SS)
▲ 美国夏威夷珍珠港

[![LSwcQg.jpg](https://s1.ax1x.com/2022/04/07/LSwcQg.jpg)](https://imgtu.com/i/LSwcQg)
▲ 上海江南造船厂

[![LSwDFP.jpg](https://s1.ax1x.com/2022/04/07/LSwDFP.jpg)](https://imgtu.com/i/LSwDFP)
▲ 广州白云机场

[![LSw0ot.jpg](https://s1.ax1x.com/2022/04/07/LSw0ot.jpg)](https://imgtu.com/i/LSw0ot)
▲ 西藏拉萨布达拉宫

[![LSwgyQ.jpg](https://s1.ax1x.com/2022/04/07/LSwgyQ.jpg)](https://imgtu.com/i/LSwgyQ)
▲ 台北圆山风景区

[![LSwrJf.jpg](https://s1.ax1x.com/2022/04/07/LSwrJf.jpg)](https://imgtu.com/i/LSwrJf)
▲ 桂林漓江风景区

[![LSwsW8.jpg](https://s1.ax1x.com/2022/04/07/LSwsW8.jpg)](https://imgtu.com/i/LSwsW8)
▲ 江苏油菜花

[![LSaa1e.jpg](https://s1.ax1x.com/2022/04/07/LSaa1e.jpg)](https://imgtu.com/i/LSaa1e)
▲ 福建宁德三都澳养殖场

[![LSwfwn.jpg](https://s1.ax1x.com/2022/04/07/LSwfwn.jpg)](https://imgtu.com/i/LSwfwn)
▲ 重庆嘉陵江口

[![LSw2Lj.jpg](https://s1.ax1x.com/2022/04/07/LSw2Lj.jpg)](https://imgtu.com/i/LSw2Lj)
▲ 长沙橘子洲

[![LSwWes.jpg](https://s1.ax1x.com/2022/04/07/LSwWes.jpg)](https://imgtu.com/i/LSwWes)
▲ 大理火烧迹地



可以通过FTP工具下载这些样例景

[![q4B8l4.jpg](https://s1.ax1x.com/2022/04/01/q4B8l4.jpg)](https://imgtu.com/i/q4B8l4)

    FTP服务器：  satapp.radi.ac.cn
    账号：  cfdata
    密码：  cfdata123
    
    目录：  temp/pkdove/

个别FTP客户端可能不好使，如果连接不上，推荐FTPRUSH下载。



---



陈甫 副研究员
中国科学院空天信息创新研究院
chenfu@aircas.ac.cn
13811147935