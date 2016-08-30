---
author: Jianlou Si
layout: post
slug: development-environment-ubuntu-eclipse-oepncv-contrib
title: 开发环境配置：ubuntu14.04 + eclipse for cpp ＋ opencv 3.1.0 ＋ opencv_contrib
categories: [ubuntu, eclipse, opencv]
tags: [ubuntu, eclipse, opencv]
---

**Table of Contents**

* TOC:
{:toc}

# 开发环境配置：
## 操作系统ubuntu14.04.4
1. 操作系统ubuntu14.04.4，安装包见附件；
## jdk
2. jdk-8u101，安装包见附件, [下载链接](http://www.oracle.com/technetwork/java/javase/downloads/jdk8-downloads-2133151.html)；
	1. 安装过程：
		- 下载安装包
		- 创建目录:

			``$ sudo mkdir /usr/lib/jvm``
      
      - 解压缩到该目录：

      		``$ sudo tar -zxvf jdk-8u101-linux-x64.tar.gz -C /usr/lib/jvm``
      
      - 修改环境变量:

      		``$ sudo vim /etc/profile``
      
      		文件的末尾追加下面内容:  
          
          ```bash
          #set oracle jdk environment
			export JAVA_HOME=/usr/lib/jvm/jdk1.8.0_101  ## 这里要注意目录要换成自己解压的jdk 目录
			export JRE_HOME=${JAVA_HOME}/jre  
			export CLASSPATH=.:${JAVA_HOME}/lib:${JRE_HOME}/lib  
			export PATH=${JAVA_HOME}/bin:$PATH  
          ```
          ``$ source /etc/profile``
		- 测试jdk
		
     		```bash
          $ java -version
          java version "1.8.0_101"
			Java(TM) SE Runtime Environment (build 1.8.0_101-b13)
			Java HotSpot(TM) 64-Bit Server VM (build 25.101-b13, mixed mode)
			```
				
	2. 安装成功
	
## eclipse－cpp－neon
3. eclipse－cpp－neon, 安装包见附件，[下载链接](http://www.eclipse.org/downloads/packages/eclipse-ide-cc-developers/neonr)；
	1. 安装过程
		- 下载安装包
		- 解压安装包
			
			``$ sudo tar -xzvf eclipse-cpp-neon-R-linux-gtk-x86_64.tar.gz -C /opt``
		- 设置环境变量
	
			``$ sudo vim /etc/profile``
      
      		文件的末尾追加下面内容:
      		
      		``export PATH=$PATH:/opt/eclipse``
      		
      		``$ source /etc/profile``
      		
		- 测试eclipse,命令行直接运行eclipse
		
			``$ eclipse``
      		
	2. 安装成功

## opencv3.1.0 及 opencv_contrib
4. opencv3.1.0 及 opencv_contrib, 源码见附件，下载链接：[opencv3.1](https://github.com/Itseez/opencv/archive/3.1.0.zip)/[opencv_contrib](https://github.com/opencv/opencv_contrib)
	1. 安装过程
		- 安装依赖库／软件包，包括
		
			```
			GCC 4.4.x or later
			CMake 2.8.7 or higher
			Git
			GTK+2.x or higher, including headers (libgtk2.0-dev)
			pkg-config
			Python 2.6 or later and Numpy 1.5 or later with developer packages (python-dev, python-numpy)
			ffmpeg or libav development packages: libavcodec-dev, libavformat-dev, libswscale-dev
			[optional] libtbb2 libtbb-dev
			[optional] libdc1394 2.x
			[optional] libjpeg-dev, libpng-dev, libtiff-dev, libjasper-dev, libdc1394-22-dev
			```
			命令行安装：
			
			```
			[compiler] $ sudo apt-get install build-essential
    		[required] $ sudo apt-get install cmake git libgtk2.0-dev pkg-config libavcodec-dev libavformat-dev libswscale-dev
    		[optional] $ sudo apt-get install python-dev python-numpy libtbb2 libtbb-dev libjpeg-dev libpng-dev libtiff-dev libjasper-dev libdc1394-22-dev
			```

		- 下载并解压opencv3.1.0及opencv_contrib，我们将加压后的文件夹opencv-3.1.0和opencv_contrib拷贝到用户Documents目录下
		- 进入opencv－3.1.0文件夹中,并建立文件夹存储编译后的二进制文件
			
			```
			$ cd ./Documents/opencv-3.1.0
			$ mkdir release
			$ cd release
			```
			
		- 编译源码
		
			```
			$ cmake -D CMAKE_BUILD_TYPE=Release -D CMAKE_INSTALL_PREFIX=/usr/local -D OPENCV_EXTRA_MODULES_PATH=../../opencv_contrib/modules .. 
			```
			
		- 安装编译生成的库
		
			```
			$ make -j7
			$ sudo make install
			```
		- 配置动态链接库搜索路径
		
			``$ sudo vim /etc/ld.so.conf``
			
			添加/usr/local/lib
			
			``$ sudo ldconfig``
	2. 完成安装
