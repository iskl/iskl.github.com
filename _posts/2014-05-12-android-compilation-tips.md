---
layout: post
title: Android 源码编译的几个经验
category: 技巧
tags: [Android]
description: Android 源码编译的几个经验
---

* 源码下载，用正统的repo获取，很容易断掉，直接用国人打好的包吧。

* 4.4.2在build的时候，jdk必须是sun-jdk6,不能用sun-jdk7或者openjdk7

* 可以用`update-alternative --config java`或者`update-java-alternative`更变java环境而不用重装

* webupd8team既提供了jdk6的ppa，又提供了jdk7的ppa

* 在make之前有两步，`build/envsetup.sh`和`lunch`，其中lunch之后，emulator也配置好了，`make`后直接执行`emulator`