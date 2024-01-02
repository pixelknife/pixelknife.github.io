# SDGSAT的TIS传感器的山地制图

TIS有三个波段，不仅仅是表示亮温的高低，还能够对地物类型有更好的表达。

下图是TIS获取的原始分发产品的局部

![step1.jpg](https://s2.loli.net/2024/01/02/mfuAeJkj5cFnM6h.jpg)

对上图做图像自适应拉伸后

![step2.jpg](https://s2.loli.net/2024/01/02/utBkZrNUxl1c5w7.jpg)

上图的结果中，黑色是温度偏低的，白色是温度偏高的。这个结果和我们平时看遥感图像的感觉不符，黑色的部分是山顶，而白亮的是山脚。而且基本上是黑白色调，视觉表现较弱。

我们设计一个简单的模式调整，将黑白反向后再调整灰度、饱和度。

![step3.jpg](https://s2.loli.net/2024/01/02/ApCOe6jLydB7v2E.jpg)

上图就和常见的可见光遥感图像更加接近了。白色的是冰川，蓝黑色的是水体。可以看到山顶附近还有不少融水湖泊。

再做适当纹理增强，提高视觉清晰度。

![step4.jpg](https://s2.loli.net/2024/01/02/PryLfsBtcF9TdIg.jpg)


---

陈甫 副研究员
中国科学院空天信息创新研究院
chenfu@aircas.ac.cn
13811147935

