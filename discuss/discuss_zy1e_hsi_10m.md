# 10米76波段高分辨率高光谱产品

ZY02D(ZY1E)该系列卫星在设计的时候，有意考虑了多个传感器，多种空间分辨率、波谱分辨率的交叉辅助关系。但是目前实际应用还没有起到一体化处理的效果。

如果还是单个传感器零敲碎打，则没有发挥整个卫星的能力。如果将几个传感器联合时过于粗糙，将误差引入其中，则会影响最终的分析结果。

这系列卫星因为实际用户相对于高分系列少的多，所以关注度较低。最近我们获得了一些该卫星的样本，因此展开一些初步分析工作。

▼ 卫星的各传感器的参数列表

[![bhuIiR.png](https://s1.ax1x.com/2022/03/10/bhuIiR.png)](https://imgtu.com/i/bhuIiR)

多个传感器的全面融合首先要让各个传感器的几何位置能够高精度对齐。这里需要依次处理以下的四组配准关系。

( PAN -- (MS1 - MS2) ) --- (HSI_VN - HSI_SW)

分别先处理MS内部和HSI内部的偏差（只有移动关系），再处理PAN和MS之间的偏差，最后处理PMS和HSI之间的偏差，后两者有分辨率上的差异。

我们之前陆续对[( PAN -- (MS1 - MS2) ) ](discuss_zy1e_pms.html)以及[(HSI_VN - HSI_SW)](discuss_zy1e_hsi_reg.html)处理都做过介绍，在这两者都完成的基础上可以做最后一步即(PMS --- HSI) 。这两个因为是完全独立的传感器，所以偏差应该是最大的。



▼ 根据卫星参数直接叠放

[![qVLlR0.gif](https://s1.ax1x.com/2022/03/20/qVLlR0.gif)](https://imgtu.com/i/qVLlR0)



▼ 通过像素刻刀软件精细配准

[![qVLQGq.gif](https://s1.ax1x.com/2022/03/20/qVLQGq.gif)](https://imgtu.com/i/qVLQGq)



在几何配准完成后就可以将HSI-VN的30米76波段与MS的10米8波段融合起来。



▼ 融合后的结果和HSI对应波段比较，分辨率提高了3倍，而辐射值没有变化。

[![qZ9QJg.gif](https://s1.ax1x.com/2022/03/20/qZ9QJg.gif)](https://imgtu.com/i/qZ9QJg)



▼ 融合后的结果和MS波谱相近的波段比较，纹理没有变化，辐射值已经用HSI对应波段的予以置换。

[![qZ9lWQ.gif](https://s1.ax1x.com/2022/03/20/qZ9lWQ.gif)](https://imgtu.com/i/qZ9lWQ)



这样的结果保持了HSI的辐射值、引入了MS的高空间分辨率，形成10米76波段的高光谱高空间分辨率产品。



---



**联系方式**

陈甫 副研究员
中国科学院空天信息创新研究院
chenfu@aircas.ac.cn
13811147935