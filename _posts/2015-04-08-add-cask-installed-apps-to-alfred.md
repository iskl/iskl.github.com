---
layout: post
title: Alfred 获取 Homebrew Cask 安装软件索引
category: 技巧
tags: [Alfred, Homebrew, MacOSX]
description: Alfred 获取 Homebrew Cask 安装软件索引
---

默认情况下，用Homebrew Cask安装的软件不在Alfred的启动器索引里。

将`~/Applications`目录添加到索引，并同时添加“文件类型：软连接”到文件类型列表里，也同样解决不了问题。

我的解决方案是把`/opt/homebrew-cask/Caskroom`添加到索引列表，不知道有没有更加优雅的方式。