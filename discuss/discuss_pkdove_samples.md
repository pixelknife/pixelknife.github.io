# pkDove案例集锦

pkDove是通过像素刻刀（PixelKnife）软件对Planet的SuperDove卫星数据做的质量提升，将3米8波段的分发产品，提高到2米8波段，而且其波谱数值可以用于定量化分析。

这里的超分辨率技术是核心关键，这在之前已经做过[介绍](discuss_superdove_x2.html)。但是我们目前还是把超分的目标定在2米而不是1.5米。这有以下几点考虑：

1）3米分辨率也不是实际成像分辨率而是制图分辨率，其公布的实际成像分辨率应该是接近4米；

2）2米是我国高分系列等多数光学卫星常用的分辨率，而1.5米则几乎没有，如果联合制图实际上还需要返回2米；

3）2米输出文件相对来说文件大小不会增加太多，信息量也是充分的。

[![bce7a8.jpg](https://s1.ax1x.com/2022/03/08/bce7a8.jpg)](https://imgtu.com/i/bce7a8)
▲ SuperDove、Sentinel2的波谱关系

我们发现SuperDove对Sentinel2做了波谱映射仿真但是并不彻底，因为其中1、3、5三个波段因为在Sentinel2中没有对应波段（10/20米对应），所以应该是没有处理的，而pkDove中则根据他们和相近可见光波段的相关性也做了对应调整，使得整个波谱在数值上连续稳定，这样后续可做一些波谱上的数值分析也是可以的了。

[![q4JMFJ.jpg](https://s1.ax1x.com/2022/04/01/q4JMFJ.jpg)](https://imgtu.com/i/q4JMFJ)

▲ 左边是Planet分发的产品，其中1、3、5波段和2、4、6波段形成锯齿状的起伏，这是很不正常的，右侧是pkDove处理后的，不仅图像分辨率增强了，而且波谱数值也正常了。

我们用pkDove处理了一系列的Planet分发的整景数据产品来检验产品。因为Planet星座是由100多颗卫星组成的，所以各个卫星的成像质量差异还是比较大的，图像的模糊（散焦）程度也不同，因此我们会对整景图像的中间部分做一个测试来确定选择强弱两级超分参数（命令行中锐化参数5或者6）来处理图像，通常使用更强参数的处理结果图像上噪声可能就会更明显一些。因为原始图像有较大差异，所以最终生成的超分版也有差异，这是正常现象。



广州

http://satsee.radi.ac.cn:8080/guang/guang.html?uid=99effe40-8639-4476-ab37-0f1572a1fd86

http://satsee.radi.ac.cn:8080/guang/guang.html?uid=3ff7b91c-df86-420f-95e1-dee8337fbbc3



桂林

http://satsee.radi.ac.cn:8080/guang/guang.html?uid=3ca5e0c2-04c5-44de-8f55-45067af203ac

http://satsee.radi.ac.cn:8080/guang/guang.html?uid=78dd0ee0-93f7-4d78-a095-a05249e45216



大理

http://satsee.radi.ac.cn:8080/guang/guang.html?uid=64a81d10-b94f-4a00-bf18-6dae1726f097

http://satsee.radi.ac.cn:8080/guang/guang.html?uid=ae3dde16-096c-45fd-aa55-622da121bd65



崇左

http://satsee.radi.ac.cn:8080/guang/guang.html?uid=600cf9dc-0e78-41aa-aba5-1a8832963731

http://satsee.radi.ac.cn:8080/guang/guang.html?uid=2d574375-251c-4578-919e-2176b3a39d09



重庆

http://satsee.radi.ac.cn:8080/guang/guang.html?uid=3c0fc612-6a03-4276-baef-5bb73f281f32

http://satsee.radi.ac.cn:8080/guang/guang.html?uid=e8258963-eb53-4b7d-a5ef-aef7344645c1



钦州

http://satsee.radi.ac.cn:8080/guang/guang.html?uid=055b9de9-ec12-41d7-b243-a21f35875e89

http://satsee.radi.ac.cn:8080/guang/guang.html?uid=e31e69d1-1666-4277-bb0c-b614bfeae2fc



海花岛

http://satsee.radi.ac.cn:8080/guang/guang.html?uid=659192e2-8f93-4b5f-8779-64b1a64412c9

http://satsee.radi.ac.cn:8080/guang/guang.html?uid=72026259-3a86-40e3-bfd3-a2bf62b04969



拉萨

http://satsee.radi.ac.cn:8080/guang/guang.html?uid=d1738a1e-8f79-47ac-8ed0-6a63ea07e1e1

http://satsee.radi.ac.cn:8080/guang/guang.html?uid=d5d0afc1-f118-4f49-bbdb-5a7c6c0737a5



美国圣迭戈

http://satsee.radi.ac.cn:8080/guang/guang.html?uid=a671f7cc-b043-4ca5-ae39-870e4d28e8e3

http://satsee.radi.ac.cn:8080/guang/guang.html?uid=86abc3c0-9d8c-4df9-97a3-9f6a412b625e






---



陈甫 副研究员
中国科学院空天信息创新研究院
chenfu@aircas.ac.cn
13811147935