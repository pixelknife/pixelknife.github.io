# SDGSAT的多光谱MII传感器的清晰化



## 背景

SDGSAT的多光谱传感器是由A/B两个相机组成的，其中B相机相对A相机来说更加模糊，影响可视效果。

我们可以通过软件方法增强图像的纹理细节。



## 修正

首先存在高亮地物饱和的问题，原图上飞机这样的物体是看不出来的。先通过去饱和工具，降低整体亮度，恢复绿色和红色波段的纹理信息。

然后增加纹理边缘信息来进一步提高图像的清晰度。



[![qbReiT.jpg](https://s1.ax1x.com/2022/04/04/qbReiT.jpg)](https://imgtu.com/i/qbReiT)




A相机也可以通过这个技术提高清晰度，可以设置不同的参数。



---



陈甫 副研究员
中国科学院空天信息创新研究院
chenfu@aircas.ac.cn
13811147935
