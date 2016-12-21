---
title: TensorFlow安装
date: 2016-12-21 21:31:08
tags:
- Deep Learning
- TensorFlow
categories: Tech
description: TensorFlow安装笔记
---
之前学习主要使用Caffe，听说TensorFlow用起来更方便而且用的人也更多，所以准备学习学习TensorFlow，小小记录一下今天的安装步骤。

## 链接
* [TensorFlow下载](https://github.com/tensorflow/tensorflow/blob/master/tensorflow/g3doc/get_started/os_setup.md)
* [中文社区](http://tensorfly.cn/)
* [官网](https://www.tensorflow.org/)

## Cuda和Cudnn
* 安装Cuda，下载cudnn，将cudnn/include头文件拷入cuda/include，cudnn/lib64拷入cuda/lib64。
* 设置环境变量
```
vi .bashrc
export LD_LIBRARY_PATH=cudapath/lib64
```

## 下载安装
```
pip install tensorflow.whl --user
```