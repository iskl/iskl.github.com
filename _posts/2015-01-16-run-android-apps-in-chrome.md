---
layout: post
title: 利用 Chrome 运行 Android 应用
category: 技巧
tags: [Chrome, Android]
description: 在 Chrome 浏览器中运行 Android 应用
---

在2014年的Google IO上，Google宣布Chrome OS平台可以运行Android应用了。但其实，不在Chrome OS上，只要有Chrome浏览器，也能达到相同的效果。

假如需要一个够方便的轻量级Android虚拟机，Chrome是个不错的选择。

具体步骤为

* 安装Chrome，版本必须高于37。

* 去[这里](https://github.com/vladikoff/chromeos-apk/blob/master/archon.md)下载ARChon，这是一个apk在Chrome上的运行时环境。

* 在Chrome的扩展页面，勾选开发者模式，点击“加载正在开发的扩展程序”加载ARChon。

* 按照[这里](https://github.com/vladikoff/chromeos-apk/blob/master/README.md)的教程安装chromeos-apk工具。

* 下载要安装的程序的apk，用chromeos-apk转换成Chrome扩展。以“静读天下”为例

终端执行

    chromeos-apk 静读天下-Moon-Reader-Pro-3.0.3.apk

若出现以下提示，说明转换成功

    Directory " com.flyersoft.moonreaderp.android " created. Copy that directory onto your Chromebook and use "Load unpacked extension" to load the application.

* 在Chrome的扩展页面，点击“加载正在开发的扩展程序”加载刚刚转换出来的扩展。这里有个小技巧，一些情况下会出现报错，提示

> 无法加载以下来源的扩展程序： ~/bin/chrome.extensions/com.flyersoft.moonreaderp.android
> There is no "message" element for key extName.

这时候打开`path/to/extensions/_locales/en/messages.json`，将

    "extName": {
      "description": "Extension name",
    }

改为

    "extName": {
      "description": "Extension name",
      "message": "静读天下"
    }

再在Chrome扩展页面点“重试”即可解决问题。

* 安装完成后，直接从Launchpad就可以打开应用。运行效果如下图所示

![静读天下](/public/attachment/Snip20150117_9.png)
