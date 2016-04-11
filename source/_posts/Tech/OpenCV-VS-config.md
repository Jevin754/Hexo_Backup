---
title: OpenCV VS 配置
date: 2016-04-11 21:35:06
tags:
categories: Tech
---
OpenCV在VS工程中的配置
<!--more-->
### 配置管理器
配置x64管理器

### 选择配置平台
选择Debug或者Release进行分别进行配置

### 配置C/C++目录
#### 包含目录
“属性管理器”->“配置属性”->“VC++目录”->“包含目录”
``` cpp 
opencv_dir\build\include
```
#### 库目录
“属性管理器”->“配置属性”->“VC++目录”->“库目录”
``` cpp
opencv_dir\build\x64\vc11\lib
```

### 配置链接器
“属性管理器”->“配置属性”->“链接器”->“输入”->“附加依赖项”
用什么就添加什么就行了，一般主要用一下两个,配Release只需去除名称后面的d
``` cpp 
opencv_core2412d.lib
opencv_highgui2412d.lib
```
更多链接文件
``` cpp 
opencv_core2412d.lib
opencv_highgui2412d.lib
opencv_imgproc2412d.lib
opencv_nonfree2412d.lib
opencv_features2d2412d.lib
opencv_photo2412d.lib
opencv_calib3d2412.lib
opencv_calib3d2412d.lib
opencv_contrib2412.lib
opencv_contrib2412d.lib
opencv_core2412.lib
opencv_features2d2412.lib
opencv_flann2412.lib
opencv_flann2412d.lib
opencv_gpu2412.lib
opencv_highgui2412.lib
opencv_imgproc2412.lib
opencv_legacy2412.lib
opencv_ml2412.lib
opencv_nonfree2412.lib
opencv_objdetect2412.lib
opencv_ocl2412.lib
opencv_photo2412.lib
opencv_stitching2412.lib
opencv_superres2412.lib
opencv_ts2412.lib
opencv_video2412.lib
opencv_videostab2412.lib
opencv_gpu2412d.lib
opencv_legacy2412d.lib
opencv_ml2412d.lib
opencv_objdetect2412d.lib
opencv_ocl2412d.lib
opencv_stitching2412d.lib
opencv_ts2412d.lib
opencv_video2412d.lib
opencv_videostab2412d.lib
```
