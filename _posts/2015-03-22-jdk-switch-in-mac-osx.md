---
layout: post
title: Mac OSX 下不同版本的 JDK 管理
category: 技巧
tags: [MacOSX, Java, JVM]
description: Mac OSX 下不同版本的 JDK 管理
---

为了看JDK1.8源码，往系统中装了多个不同版本的JDK。这里对Mac OSX下的JDK安装情况和切换方法做一下记录。

10.9之后的Mac OSX自带了JDK1.6，安装在`/System`目录下

	/System/Library/Java/JavaVirtualMachines/1.6.0.jdk/`

自己从Oracle下载的JDK1.7、1.8会被安装到`/Library`目录


	/Library/Java/JavaVirtualMachines/...

切换JDK，通常的做法是

	export JAVA_HOME=JDK目录/Contents/Home

在Github上发现了一个叫Jenv的工具，可以方便切换不同版本JDK。

安装：

	brew install jenv
	echo 'export PATH="$HOME/.jenv/bin:$PATH"' >> ~/.bash_profile
	echo 'eval "$(jenv init -)"' >> ~/.bash_profile

添加JDK：

	jenv add /System/Library/Java/JavaVirtualMachines/1.6.0.jdk/Contents/Home
	jenv add /Library/Java/JavaVirtualMachines/jdk1.7.0_75.jdk/Contents/Home/
	jenv add /Library/Java/JavaVirtualMachines/jdk1.8.0_40.jdk/Contents/Home/

列举所有JDK：

	jenv versions

切换JDK：

	jenv global 1.6
	jenv global 1.7
	jenv global 1.8

[more](http://www.jenv.be/)