---
layout: post
title: fish 下使用 rvm
category: 技巧
tags: [fish, rvm, shell]
description: fish 中使用 rvm
---

由于fish不兼容bash中`expoet`、`alias`的用法，默认不会执行`.bashrc`、`.bash_profile`等文件，所以rvm在fish下默认不生效。

通过以下办法解决

	curl -L --create-dirs -o ~/.config/fish/functions/rvm.fish https://raw.github.com/lunks/fish-nuggets/master/functions/rvm.fish

fish启动时会自动加载配置目录中的`config.fish`和子目录`functions`下的文件。`rvm.fish`实现了rvm的环境配置。

另外，安装rvm需要在bash下进行，fish下安装rvm会报错。

