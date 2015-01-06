---
layout: post
title: 让 Finder 标题栏显示完整路径
category: 技巧
tags: [Finder, MacOSX]
description: 让Finder的标题栏显示完整路径
---

终端中输入

	defaults write com.apple.finder _FXShowPosixPathInTitle -bool YES

重启Finder