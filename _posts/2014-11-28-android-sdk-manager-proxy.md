---
layout: post
title: 解决 Android SDK Manager 无法更新问题
category: 技巧
tags: [Android, 代理]
description: 为Android SDK Manager配置代理
---

1. 打开Performances菜单，将“Proxy Settings”里的“HTTP Proxy Server”和“HTTP Proxy Port”分别设置成`mirrors.neusoft.edu.cn`和`80`

1. 将Others中的“Force https://...sources to be fetched using http://...”复选框勾上

![附图](/public/attachment/Snip20150102_5.png)