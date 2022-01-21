# 基于公开数据的5米影像地图

欧空局的哨兵二号卫星是目前使用率最高的公开数据源，它的两个卫星可以使得访问时间频率达到5天一次，几何定位非常准确，而且完备的波段组合也能够制作排除大气干扰的辐射校正产品。但是它的空间分辨率有限，其中可见光和近红外波段4个波段是10米，还有5个红边和短波红外波段是20米，对于影像地图来说还是有所不足。

我们通过一系列图像处理方法，将原来10米/20米的空间分辨率做一定的提升，将制图分辨率提高到一倍，形成5米9波段的数据集。

比较处理前后的波段组合图像

[![7WwEi4.jpg](https://s4.ax1x.com/2022/01/21/7WwEi4.jpg)](https://imgtu.com/i/7WwEi4)
▲波段组合321，可见光

[![7WwiZT.jpg](https://s4.ax1x.com/2022/01/21/7WwiZT.jpg)](https://imgtu.com/i/7WwiZT)
▲波段组合543，近红外-红边-红

[![7WwCLV.jpg](https://s4.ax1x.com/2022/01/21/7WwCLV.jpg)](https://imgtu.com/i/7WwCLV)
▲波段组合987，短波红外-近红外

比较处理前后的每个波段

[![7WwVJJ.jpg](https://s4.ax1x.com/2022/01/21/7WwVJJ.jpg)](https://imgtu.com/i/7WwVJJ)
▲波段1（原波段2）

[![7WwZW9.jpg](https://s4.ax1x.com/2022/01/21/7WwZW9.jpg)](https://imgtu.com/i/7WwZW9)
▲波段2（原波段3）

[![7WwnQ1.jpg](https://s4.ax1x.com/2022/01/21/7WwnQ1.jpg)](https://imgtu.com/i/7WwnQ1)
▲波段3（原波段4）

[![7WwezR.jpg](https://s4.ax1x.com/2022/01/21/7WwezR.jpg)](https://imgtu.com/i/7WwezR)
▲波段4（原波段5）

[![7Wwusx.jpg](https://s4.ax1x.com/2022/01/21/7Wwusx.jpg)](https://imgtu.com/i/7Wwusx)
▲波段5（原波段6）

[![7WwQeK.jpg](https://s4.ax1x.com/2022/01/21/7WwQeK.jpg)](https://imgtu.com/i/7WwQeK)
▲波段6（原波段7）

[![7WwldO.jpg](https://s4.ax1x.com/2022/01/21/7WwldO.jpg)](https://imgtu.com/i/7WwldO)
▲波段7（原波段8）

[![7WwFdU.jpg](https://s4.ax1x.com/2022/01/21/7WwFdU.jpg)](https://imgtu.com/i/7WwFdU)
▲波段8（原波段11）

[![7WwkoF.jpg](https://s4.ax1x.com/2022/01/21/7WwkoF.jpg)](https://imgtu.com/i/7WwkoF)
▲波段9（原波段12）


这样的处理，并没有增加图像的信息，但是对于一些纹理细节有所突出，对于图像的可视效果有所提高。

可以在5米尺度上制作全国的时序影像地图(之前我们制作了[2020年10米36帧北京时序](../product/product_cloudless_world.html))，既没有源数据的成本，也能够满足普通网友了解地表动态变化的基本需要。


---

**联系方式**

陈甫 副研究员
中国科学院空天信息创新研究院
chenfu@aircas.ac.cn
13811147935

