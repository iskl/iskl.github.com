---
layout: post
title: Trac 安装备忘录
category: 技巧
tags: [Trac, Python]
description: Trac 安装备忘录
---

1. `Babel`版本必须为`0.9.6`，高版本会导致多国语言功能不可用，血的教训。‘pip install -v Babel==0.9.6`
2. 安装插件后需要更新数据库结构，操作为`trac-admin path/to/trac/ upgrade`
3. 刷新数据库后任然报错，则重启Apache2服务