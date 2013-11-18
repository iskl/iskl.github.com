---
layout: post
title: 关闭rpimonitor的包升级检测
category: tip
description: 修改SHOW_PACKAGE_UPDATE为0；删除updatestatus.txt
---

    sudo vim /etc/default/rpimonitor 

修改SHOW_PACKAGE_UPDATE为0.

    sudo rm /usr/share/rpimonitor/updatestatus.txt