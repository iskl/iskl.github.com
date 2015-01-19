---
layout: post
title: 用 HSDB 探索 HotSpot 运行时数据
category: 技巧
tags: [Java, HotSpot]
description: 用 HSDB 分析 HotSpot 虚拟机内存
---

用jdb或者IntelliJ Idea的调试器暂停程序

打开HSDB，注意权限

    sudo java -cp /Library/Java/JavaVirtualMachines/jdk1.7.0_71.jdk/Contents/Home/lib/sa-jdi.jar sun.jvm.hotspot.HSDB

在活动监视器中查看程序PID，File -> Attach to HotSpot Process，输入PID，attach上。