---
layout: post
title: 在 Cygwin 中安装包管理工具 apt-cyg
category: 技巧
tags: [Cygwin, apt-cyg]
description: apt-cyg的安装
---

首先用Cygwin自带的安装工具安装上subversion和wget

然后执行

	svn --force export http://apt-cyg.googlecode.com/svn/trunk/ /bin/
	chmod +x /bin/apt-cyg

apt-cyg的使用方法和apt-get类似，主要命令有

> `apt-cyg install <package names>` install packages
> `apt-cyg remove <package names>` remove packages
> `apt-cyg update` update setup.ini
> `apt-cyg show` show installed packages
> `apt-cyg find <pattern(s)>` find packages matching patterns
> `apt-cyg describe <pattern(s)>` describe packages matching patterns
> `apt-cyg packageof <commands or files>` locate parent packages 

[apt-cyg homepage](https://code.google.com/p/apt-cyg/)