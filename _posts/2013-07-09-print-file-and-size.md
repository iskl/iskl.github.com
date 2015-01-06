---
layout: post
title: tree 命令附带文件大小
category: 技巧
tags: [Shell, tree]
description: tree -h
---

tree命令能很清晰地生成目录的树结构，若要附带上文件大小的显示，只需执行

    tree -h

`-h`意为更加人性化的`-s`，每个文件名旁所附带的size由KB、MB、GB做单位，
并且自动设置好了对齐。