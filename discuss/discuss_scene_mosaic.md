# 大幅面多景镶嵌



## 1）每景都做好正射工作

目前我们用的工具是ENVI上的RPC正射工具，目前来看误差还是不小，需要每景检测。这里误差来自几个方面，卫星提供的RPC文件本来就有误差，DEM精度也不够，自动找的控制点的精度和数量不够。



## 2）制作成标注化的16位TIFF图像

因为处理可能涉及很多软件，所以会对图像的一些性质有所变化
这里的标注图像，有几个要点：

* 设置透明色0, "-a_nodata 0"
* RGB三波段，把各个波段的描述明确定义。（如果有所差异，gdalbuildvrt无法准确运行）, "-co photometric=rgb -colorinterp red,green,blue"
* 将亮度空间调到0-65535，"-scale 0 1024 0 65536"
* 使用瓦块，"-co tiled=yes"
* 考虑使用一定压缩格式 "-co compress=lzw"，发现GDAL有时候无法读取PS生成的compress=deflate的格式，虽然deflate的压缩率确实更高一些。
* 使用bigtiff格式，”-co bigtiff=yes"


命令行批处理（用新GDAL）样例：

    MD RGB
    
    FOR /F %I IN ('DIR GF*_PMS*.TIF /B') DO gdal_translate -a_nodata 0 -co photometric=rgb -colorinterp red,green,blue -scale 0 1024 0 65536 -co tiled=yes -co compress=lzw -co bigtiff=yes %I rgb\%I



## 3）同轨道的拼接

这里用拼接这个词，和镶嵌概念有所区分。这里说的是一个连续轨道上的多景有交叠区域的景之间的拼接。

因为处理算法的关系，图像周边可能有几个像素的黑边。可以通过向景缩小若干像素（20个？）。如果相邻两景正射后的偏差不超过一个像素，那么即使是简单gdalbuildvrt的前后叠放，也可以让客户难以看到边界。

photoshop中可以用几个操作来简单实现，将这组操作命名为shrink动作。



## 4）缩略图调色

以64米为一个基准尺度，这个是2米的32倍，是0.8米的80倍，是0.5米的128倍。

通过gdaladdo和gdal_translate制作64米分辨率的缩略图。

GE上有landsat的2020年数据，64米是L8的最高分辨率15米的4倍。根据待调色的图像缩略图的坐标，将事先下载的LS2020的相关区域图像生成出来。

可以通过将缩略图简单快速的增强，然后在PS中用铅笔工具（硬度100%）给那些认为是晴空的地物加以标注。

将标红的区域的待调色部分和LS2020部分比较，通过均值和方差的简单变化，将颜色调整到和标注图像接近，基本上解决了白平衡问题。而且通过这样一个参考底图，让制作大幅面图像的各个部分的颜色都设置在比较理想的位置上。

高分图像有所谓的肥尾现象，为了保证高亮的建筑区域的纹理，先做一个全局的指数化调整，类似PS上的曲线调整。然后还可以利用高亮区域的局部积聚特性，可以做局部的直方图调整，进一步恢复高亮区域纹理。



## 5）matlab工具处理步骤

path_composite 建构轨道，建构VRT文件
proc_composite  建构批处理

step1 建立缩略图

mark 用PS标红

wb_exp 白平衡和全局指数指数亮度调整

photoshop fill-target 填充成完整的缩略图，缩略图确定调色目标

step2 调色工具、去饱和工具



---

**联系方式**

陈甫 副研究员
中国科学院空天信息创新研究院
chenfu@aircas.ac.cn
13811147935
