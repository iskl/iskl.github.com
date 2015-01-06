---
layout: post
title: transmission 目标文件夹的用户组要求
category: 技巧
tags: [transmission, Shell]
description: sudo chmod -R debian-transmission:debian-transmission
---

transmission正在下载的临时文件必须是`debian-transmission`用户组的`debian-transmission`用户所属，不然会出现因权限错误而无法写入文件的报错。

在临时下载文件夹执行

    sudo chmod -R debian-transmission:debian-transmission *

其中，`-R`指文件夹递归