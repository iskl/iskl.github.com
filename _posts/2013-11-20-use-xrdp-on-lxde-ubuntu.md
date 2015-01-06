---
layout: post
title: 在 LXDE Ubuntu 中启用 xrdp 远程控制
category: 技巧
tags: [Ubuntu, xrdp, LXDE]
description: echo lxsession -s Lubuntu -e LXDE > ~/.xsession
---

默认安装的xrdp打开的是Gnome的session，指定使用LXDE的办法是

    echo lxsession -s Lubuntu -e LXDE > ~/.xsession
