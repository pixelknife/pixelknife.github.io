# 视觉超分辨率


遥感对于分辨率的要求可以说是永无止境的，特别是空间分辨率。在浏览一副影像的时候，人们总是从缩略图推进到全分辨率感受逐渐清晰的一个过程，在此基础上仍然意犹未尽，总想试试能否看的更清楚一些。这时候有的看图软件不允许再放大，有的软件只能给出一个模糊的放大插值的图。

我们提供的工具可以在全分辨率的基础上再放大一个层次，将视觉分辨率提高一倍，以满足观众的视觉需求。这并没有实质性增加图像内在包含的信息量，但是确实可以增加直接投送给观众的信息量，这在制图以及目视判图的时候还是很有用的。

下面的案例中，第一行是在Photoshop中将图像放大一倍后的模糊图像作为参考，第二行是通过我们的像素刻刀软件制作出来的视觉分辨率提高一倍的图像。

▼SKYSAT，模糊的0.5米到清晰的0.25米

[![IIurkR.jpg](https://z3.ax1x.com/2021/11/17/IIurkR.jpg)](https://imgtu.com/i/IIurkR)

▼ 高分七号（全色0.6米多光谱2.4米），融合结果从模糊的0.6米到清晰的0.3米

[![I4UfPg.jpg](https://z3.ax1x.com/2021/11/17/I4UfPg.jpg)](https://imgtu.com/i/I4UfPg)

▼ 高分一号B（全色2米多光谱8米），PAN从模糊的2米到清晰的1米

[![I50QEt.jpg](https://z3.ax1x.com/2021/11/17/I50QEt.jpg)](https://imgtu.com/i/I50QEt)

▼ 高分六号（全色2米多光谱8米），融合结果从模糊的2米到清晰的1米

[![I4GdeS.jpg](https://z3.ax1x.com/2021/11/17/I4GdeS.jpg)](https://imgtu.com/i/I4GdeS)


▼ 哨兵二号，可见光部分为10米，增强到5米

[![I4Gwdg.jpg](https://z3.ax1x.com/2021/11/17/I4Gwdg.jpg)](https://imgtu.com/i/I4Gwdg)

▼SUOMI NPP，夜光月度产品，从500米增强到250米

[![IIQl0e.jpg](https://z3.ax1x.com/2021/11/17/IIQl0e.jpg)](https://imgtu.com/i/IIQl0e)


这里增强的程度是可以用参数调节的。这个调节的程度取决于源图像的质量，如果源图像比较模糊就可以用较大的参数。还有一点值得注意，如果源图像已经经过了图像压缩、解压缩或者MTF增强以后就不一定适用这个超分辨率，因为图像可能已经引入了一些额外的噪声，后续如果继续增强，可能会把噪声进一步放大，影响视觉效果。





---

**联系方式**

陈甫 副研究员
中国科学院空天信息创新研究院
chenfu@aircas.ac.cn
13811147935

