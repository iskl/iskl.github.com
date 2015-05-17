---
layout: post
title: 非越狱 iOS 科学上网总结
category: 技巧
tags: [科学上网, Shadowsocks, iOS]
description: iOS科学上网总结
---

在不越狱的情况下，iOS无法实现Android般完美的科学上网，以下方式有各自的优缺点。

1. Shadowsocks.app，直接从App Store安装。优点，简单方便，可同时用于WiFi模式和4G模式；缺点，需要自建Shadowsocks服务器，只能在应用内科学上网。
2. 利用pac。优点，简单方便；缺点，只有WiFi下支持pac，需要自己部署服务器或使用曲径等付费服务。
3. 结合Shadowsocks.app和pac。优点，能部分地实现所有app科学上网；缺点，限制很大，不越狱的情况下，Shadowsocks.app只能在后台保持几分钟。
4. 路由器端科学上网。优点，对iOS设备来说透明；缺点，只适用于WiFi模式
5. Android设备和iOS设备同时连接到一个热点，Android设备通过fqrouter2科学上网，并将pac分享给iOS使用。相比方法2、3，优点，实现简单；缺点，只适用于WiFi模式，需要随时携带Android设备。。。

个别典型应用，可以用一些特定的方法实现科学上网。

1. Gmail或Google Apps的邮箱功能，可通过CloudMagic或者Mailbox中转。推荐前者，中国区App Store有售，个人感觉体验比后者好。
2. Gmail通信录，可以通过App Store上一大堆同步Gmail通信录和iCloud通信录的app实现。
3. Google Calendar和Task，已弃，转投iCloud。OS X和iOS下的Fantastical很好用，Android设备下可通过CalDAV-Sync和JB Workaround实现iCloud日程历的同步更新，不过操作神烦，我不会去部署第二次了。