---
layout: post
title: 使screen在Putty中也能正常滚屏
category: tip
description: termcapinfo xterm|xterms|xs ti@:te=\E[2J
---

编辑/etc/screenrc，添加以下一行代码到最后

    termcapinfo xterm|xterms|xs ti@:te=\E[2J

另外，在screenxia，快捷键`Ctrl+A+[`可进入选择模式上下滚屏，`PageUp`和`PageDown`可用。