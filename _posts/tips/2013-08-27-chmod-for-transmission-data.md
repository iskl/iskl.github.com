---
layout: post
title: transmission临时下载文件须赋予特定用户组
category: tip
description: sudo chmod -R debian-transmission:debian-transmission 
---

transmission正在下载的临时文件必须是debian-transmission用户组的debian-transmission用户所属，不然会出现因权限错误而无法写入文件的报错。

在临时下载文件夹执行

    sudo chmod -R debian-transmission:debian-transmission *

其中，-R指文件夹递归