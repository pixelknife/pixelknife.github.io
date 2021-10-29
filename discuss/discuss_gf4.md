# 高分四号质量提升

高分四号是目前一个适合用于大范围的自然灾害监测的工具。高分四号是一颗科研星，而且是这一类型的第一颗，因此目前还是存在不少通过处理软件提升图像质量的空间。



## 火点提取

高分四号的IRS中红外传感器对地表高温敏感，专门用于火情监控。但是IRS存在大量的椒盐噪声，在做小型火点提取的时候会有一定的混淆。

这有两种解决思路，一个是单景中自适应测定阈值来区分噪声和信号，并且使用数字形态学方法来区分单个的噪点。另外一个是没隔一段时间做一次夜间的拍摄统计，这样的噪声在一定时间期比较稳定，然后在图像中对这些标识出来的像素点用周边插值替代。

[![5OHnC8.jpg](https://z3.ax1x.com/2021/10/29/5OHnC8.jpg)](https://imgtu.com/i/5OHnC8)
▲原始的IRS图像

[![5OHe4f.png](https://z3.ax1x.com/2021/10/29/5OHe4f.png)](https://imgtu.com/i/5OHe4f)
▲提取高温点后的图像



## 清晰度提升

高分四号PMS传感器的标准分辨率是50米，但是因为散焦等原因，图像会更加模糊。通过像素刻刀(PixelKnife)软件可以恢复一定的清晰度。

[![5OHCge.jpg](https://z3.ax1x.com/2021/10/29/5OHCge.jpg)](https://imgtu.com/i/5OHCge)
▲原始的RGB图像

[![5O7vAx.jpg](https://z3.ax1x.com/2021/10/29/5O7vAx.jpg)](https://imgtu.com/i/5O7vAx)
▲清晰度提升后的RGB图像

[![5O7XH1.jpg](https://z3.ax1x.com/2021/10/29/5O7XH1.jpg)](https://imgtu.com/i/5O7XH1)
▲清晰度提升，并且加入近红外波段成分

[![5OXXHH.jpg](https://z3.ax1x.com/2021/10/29/5OXXHH.jpg)](https://imgtu.com/i/5OXXHH)
▲进一步调整，削弱大气的影响

---

**联系方式**

陈甫 副研究员
中国科学院空天信息创新研究院
chenfu@aircas.ac.cn
13811147935

