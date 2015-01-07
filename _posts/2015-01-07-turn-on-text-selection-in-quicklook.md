---
layout: post
title: 开启 Quicklook 中的文本选择功能
category: 技巧
tags: [Quicklook, MacOSX]
description: 开启Quicklook中的文本选择功能
---

终端运行

	defaults write com.apple.finder QLEnableTextSelection -bool true

然后重启Finder

	killall Finder