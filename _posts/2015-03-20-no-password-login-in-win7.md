---
layout: post
title: Mac OSX 下 Win7 虚拟机免密登陆
category: 技巧
tags: [MacOSX, Windows]
description: Mac OSX 下 Win7 虚拟机免密登陆
---

Parallels Desktop虚拟机设计得很人性化，默认配置了文件系统与操作的诸多共享，将宿主Mac系统与Win虚拟机打通，无缝切换。

有一个略显麻烦的地方，当虚拟机自动启动时，需要用户输入密码。可以通过在Win7中设置免密登陆去除这个过程。

开始菜单搜索栏输入`netplwiz`，弹出高级用户账户对话框，去除“要使用本机，用户需输入用户名和密码”的勾选，批准UAC提权，完成。