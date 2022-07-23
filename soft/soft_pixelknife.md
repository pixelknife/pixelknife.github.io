# 像素刻刀(PixelKnife)软件

像素刻刀软件是为了处理大型遥感卫星数据、特别是中国国产遥感卫星数据而开发的一系列重要的软件算法工具的集合。



## 1 软件功能

软件的理念是从解决实际工程问题出发，而且根据二八原则，力图解决其中的最核心的问题。

处理的数据对象以高分系类卫星为主，当然其他卫星或多或少也有这样一些问题。



### 1.1 [高精度配准](algorithm/algorithm_registration.html)

### 1.2 [不失真融合](algorithm/algorithm_recover.html)

### 1.3 [缩略图调色](algorithm/algorithm_thumb.html)

### 1.4 [无饱和增强](algorithm/algorithm_deexpose.html)

### 1.5 [自动变化检测](algorithm/algorithm_change_detect.html)

### 1.6  [纹理保真锐化](algorithm/algorithm_unsharp.html)

### 1.7  [纹理保真锐化](algorithm/algorithm_fine_tdt_landsat.html)


## 2 配置环境

### 硬件环境

内存是一个关键要求：**电脑需具备16GB内存**。
适当注意硬盘空间：每个GF1融合复原结果为3GB，每个GF2融合复原结果为8GB。
估计执行时间（在普通PC或笔记本）：GF1一景5分钟、GF2一景15分钟。

实际测试用例：
电脑配置：windows 7 64位系统  intel core i7-6700 @3.4GHz  内存16GB
GF1： 263秒
GF2： 813秒

### 软件环境

本软件在64位的WINDOWS系统上工作，需要vs2013的runtime运行库。
本软件是绿色软件，即不需要复杂的安装卸载步骤，用户只需要将安装包直接解压在指定的位置即可。



## 3 DEMO版本

DEMO版和正式版的差别在于DEMO版上生成的图像中有水印痕迹。

[下载和使用](https://www.zybuluo.com/novachen/note/426294)



---

**联系方式**

陈甫 副研究员
中国科学院空天信息创新研究院
chenfu@aircas.ac.cn
13811147935

