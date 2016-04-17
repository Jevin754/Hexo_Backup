---
title: Hexo+Github 配置
date: 2016-04-12 09:23:40
tags: Hexo
categories: Tech
description: 这篇博文主要介绍Hexo在Windows和Ubuntu下的配置
---
折腾了几天，终于把Hexo在Ubuntu和Windows下的环境配好，个人博客搭建完成。
## 环境配置
### Ubuntu

#### 安装Nodejs
  从[Nodejs官网](https://nodejs.org/en/)下载合适的版本，我使用的方法是源码编译安装，下载“Source Code”，解压，安装：
  ``` bash
  ./configure
  make
  sudo make install
  ```
  安装完成后查看是否安装成功
  ``` bash
  node -v
  ```
#### 安装npm
  npm是Nodejs的包管理工具，只需要输入一下一行命令
  ``` bash
  curl http://npmjs.org/install.sh | sudo sh 
  ```
#### 安装Hexo
  如果npm速度较慢，可以换淘宝源：http://npm.taobao.org/
  ``` bash
  nmp install hexo-cli -g --registry=https://registry.npm.taobao.org
  ```

### Windows
#### 安装Git
  安装Git有几种方法

  方法1：
  从[Git官网](https://git-for-windows.github.io/)下载合适版本安装。

  方法2：
  如果你是Cygwin用户，可以直接在Cygwin里安装Git。
#### 安装Nodejs
  从[Nodejs官网](https://nodejs.org/en/)下载合适的版本，直接安装。
#### 安装Hexo
  直接在Git Bash或者Cygwin输入命令：
  ``` bash
  npm install -g hexo
  ```

  至此，Windows和Ubuntu下的环境配置完成。

## 博客搭建
### 建站
  执行以下命令，Hexo将在指定文件夹中创建所需文件。
  ``` bash
  hexo init <folder>
  cd <folder>
  npm install
  ```
### 修改配置
  主要修改一下配置：
  ``` bash
  url: # e.g. 输入 http://username_github.github.io

  new_post_name: :year/:month/:title.md # 方便管理_post文件夹

  deploy:
  type: git
  repository: git@github.com:Github用户名同名仓库
  branch: master
  ```
### 使用主题
  Github上有很多Hexo主题，可以参考这个[链接](https://github.com/hexojs/hexo/wiki/themes)，个人觉得用得比较多的是Coney。
  可以直接
  ``` bash
  git clone resp@name
  ```
  或者直接下载下来解压到theme目录下。
  先修改Hexo配置文件，将theme改成你要使用的主题名称，然后就是修改主题的配置，打开_config.yml进行修改。
  主题支持Disqus和多说评论，任选一个喜欢的添加就好，还有各种统计工具，比如Google Analysis等。

### Hexo常用命令
  ``` bash
  # 建站
  hexo init <folder>
  cd <folder>
  npm install
 
  # 文章
  hexo new page "page_name" # 新建页面
  hexo new "file name" # 新建博文
  hexo new draft "file name" # 新建草稿
  
  # 部署
  hexo g # 即 hexo generate 生成
  hexo d # 即 hexo deploy 部署
  
  # 清除
  hexo clean
  ```

## 不同平台的同步
Hexo在不同平台同步时，可以在根目录下新建git仓库，将整个文件夹数据同步至Github。
修改根目录下的.gitignore文件
```
public/
/.deploy_git/
```
每次更新完博客之后进行同步就OK了。

## 关于图床
七牛图片[基本处理](http://developer.qiniu.com/code/v6/api/kodo-api/image/imageview2.html)