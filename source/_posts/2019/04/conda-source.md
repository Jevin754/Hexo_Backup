---
title: Conda源
date: 2019-04-26 13:35:58
tags: conda
categories: Tech
description: Conda国内源
---
Conda国内源配置。（科大源和清华源已经暂时停更）

## 科大源
* [科大源使用帮助](http://mirrors.ustc.edu.cn/help/anaconda.html)
``` bash
conda config --add channels https://mirrors.ustc.edu.cn/anaconda/pkgs/free/
conda config --add channels https://mirrors.ustc.edu.cn/anaconda/pkgs/main/
conda config --set show_channel_urls yes

# 附加库
conda config --add channels https://mirrors.ustc.edu.cn/anaconda/cloud/conda-forge/
conda config --add channels https://mirrors.ustc.edu.cn/anaconda/cloud/msys2/
conda config --add channels https://mirrors.ustc.edu.cn/anaconda/cloud/bioconda/
conda config --add channels https://mirrors.ustc.edu.cn/anaconda/cloud/menpo/
```

## 腾讯源
* [腾讯源使用帮助](https://mirrors.cloud.tencent.com/help/Anaconda.html)
``` bash
conda config --add channels http://mirrors.cloud.tencent.com/anaconda/pkgs/free/
conda config --add channels http://mirrors.cloud.tencent.com/anaconda/pkgs/main/
conda config --set show_channel_urls yes

# 附加库
conda config --add channels http://mirrors.cloud.tencent.com/anaconda/cloud/conda-forge/
conda config --add channels http://mirrors.cloud.tencent.com/anaconda/cloud/msys2/
conda config --add channels http://mirrors.cloud.tencent.com/anaconda/cloud/bioconda/
conda config --add channels http://mirrors.cloud.tencent.com/anaconda/cloud/menpo/
```

## 常用命令
``` bash
# 查看源
conda config --show channels

# 删除channel，使用默认源
conda config --remove-key channels
```