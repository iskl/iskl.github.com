---
layout: post
title: GoFlex Home 常用 Hack 操作
category: 技巧
tags: [GoFlexHome, NAS]
description: 
---

## SSH控制

	ssh kailai_hipserv2_seagateplug_OOXX-OOXX-OOXX-OOXX@NASIPADDRESS -p 22

其中，`OOXX-OOXX-OOXX-OOXX`是NAS底部铭牌上德序列号
 
## 安装ipkg

参照[这篇文章](http://www.openstora.com/wiki/index.php?title=Installing_a_package_manager)
 
## 设置PATH

	sudo /opt/bin/nano /etc/environment
	PATH=/usr/local/bin:/usr/bin:/bin:/opt/bin:/usr/sbin:/opt/sbin:/usr/sbin:/sbin:/opt/local/bin
 
## 安装python

	sudo ipkg install python27
	ln -s python python2.7
 
## 安装py27_setuptools

	sudo ipkg install py27_setuptools
 
## 安装pip

参照[这篇文章](http://www.pip-installer.org/en/latest/installing.html)

	curl -O https://raw.github.com/pypa/pip/master/contrib/get-pip.py -k
	sudo python get-pip.py