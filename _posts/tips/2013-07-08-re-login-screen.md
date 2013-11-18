---
layout: post
title: 恢复screen会话
category: tip
description: 先执行screen -d断掉会话
---

一般情况下，在shell中

    screen -r

可以恢复出上次Putty断线时的会话屏幕，但有时这么做只显示"有会话还连着，没有什么可恢复的"（大意）。
这时候需要先执行

    screen -d

断掉会话，再执行`-r`即可切换到上次退出的会话。