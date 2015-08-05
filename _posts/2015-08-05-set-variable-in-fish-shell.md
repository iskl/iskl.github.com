---
layout: post
title: fish shell 下添加变量
category: 技巧
tags: [fish]
description: fish shell 下添加变量
---

```
$ touch ~/.config/fish/config.fish
$ echo "set -gx PATH \$PATH <path>" >> ~/.config/fish/config.fish
```