---
layout: post
title: 在LXDE Ubuntu中使用xrdp
category: tip
description: echo lxsession -s Lubuntu -e LXDE > ~/.xsession
---

默认安装的xrdp打开的是Gnome的session，指定使用LXDE的办法是

    echo lxsession -s Lubuntu -e LXDE > ~/.xsession

其实就是在用户目录下新建`.xsession`文件，写入`lxsession -s Lubuntu -e`