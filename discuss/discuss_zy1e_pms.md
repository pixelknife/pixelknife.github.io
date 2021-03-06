# ZY1E初探之一：2.5米8波段全色多光谱相机


首先介绍一下这个卫星的基本信息。资源一号02D(ZY1E)卫星又称为5米光学卫星，是中国空间基础设施规划中的重要型号，由国家自然资源部牵头负责项目建设，由中国航天科技集团有限公司所属上海航天技术研究院研制。2019年9月12日11时26分，中国在太原卫星发射中心用长征四号乙运载火箭，成功将资源一号02D卫星发射升空，卫星顺利进入预定轨道。

这颗卫星虽然叫5米光学卫星，但是实际上有两个传感器，一个是2.5/10米8波段的多光谱相机，一个是高光谱相机。这是因为这个卫星规划的比较早，后来技术进步了，设计的时候把指标提高了。

[![bhuIiR.png](https://s1.ax1x.com/2022/03/10/bhuIiR.png)](https://imgtu.com/i/bhuIiR)

这里表格上多光谱是9个波段，其中第一个是2.5米的全色波段，后面8个是10米的多光谱波段。

对于大家更熟悉的多光谱相机来说，这个新传感器相对于相似的高分1和高分6来说，幅宽提高到115公里，波段增加了四个。

但是这增加的四个新波段，有点勉强，因为它们不是同时同角度成像的。举一下实例，543波段和987波段组合的切换比较。

[![bhu7z6.gif](https://s1.ax1x.com/2022/03/10/bhu7z6.gif)](https://imgtu.com/i/bhu7z6)

可以看到云的运动非常显著，说明成像的时间差的比较多。而且仔细看山体部分有变形差异，说明成像的角度有偏差。

再做一个跨前4波段和后4波段的组合，将958三个近红外范围的波段形成组合。

[![bhubQK.png](https://s1.ax1x.com/2022/03/10/bhubQK.png)](https://imgtu.com/i/bhubQK)


可以看到这里在一些明暗边缘有红眼皮现象（就是波段之间没有配准）。其中云的部分是拍摄时间偏差导致的，没有办法的。而其他地物是因为成像角度偏差导致的。这样原来落到一个坐标上的8个波段其实反映的不是同一处地物的特性，那么会给分析带来误差。

我开发的像素刻刀(PixelKnife)可以克服任意的非线性变形，只要用点计算时间就可以把这个偏差纠正回来。这个情况和之前高分二号之类的情况是类似的。

[![bhuLLD.png](https://s1.ax1x.com/2022/03/10/bhuLLD.png)](https://imgtu.com/i/bhuLLD)


我们把两个状态切换显示比较一下。

[![bhujdH.gif](https://s1.ax1x.com/2022/03/10/bhujdH.gif)](https://imgtu.com/i/bhujdH)


为啥我们要对多光谱MUX传感器中一两个像素的偏差这么重视呢，因为这后面还要和搞分辨率的全色波段PAN做融合。在MUX上一个像素的偏差，会导致在融合结果上4个像素的怪异色彩，比如出现红色的道路什么的。

融合的时候还要将PAN和MUX做一次配准，然后融合的结果就符合比较理想了。

通过像素刻刀工具完成的融合结果，显示其中的958波段组合。

[![bhuXee.jpg](https://s1.ax1x.com/2022/03/10/bhuXee.jpg)](https://imgtu.com/i/bhuXee)

如果不是跨两组波段的情况，那么云的部分不会出现红眼皮现象，比如432真彩色。

[![bhuqsO.jpg](https://s1.ax1x.com/2022/03/10/bhuqsO.jpg)](https://imgtu.com/i/bhuqsO)

比如987波段组合

[![bhuoJ1.jpg](https://s1.ax1x.com/2022/03/10/bhuoJ1.jpg)](https://imgtu.com/i/bhuoJ1)

利用这个数据构图的时候可能要注意一下这些特殊情况，以达到最好的显示效果。

下次再介绍一下ZY1E上的高光谱相机的情况。

---

陈甫 副研究员
中国科学院空天信息创新研究院
chenfu@aircas.ac.cn
13811147935





