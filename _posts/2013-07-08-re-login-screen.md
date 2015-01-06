---
layout: post
title: 恢复 screen 会话
category: 技巧
tags: [Shell, screen]
description: 先执行screen -d断掉会话
---

先执行

    screen -d

切掉未断开的会话，再执行

	screen -r

连接会话。