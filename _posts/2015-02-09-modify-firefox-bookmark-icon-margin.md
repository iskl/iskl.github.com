---
layout: post
title: Firefox 中修改书签栏图标间距
category: 技巧
tags: [Firefox]
description: Firefox 中修改书签栏图标间距
---

相比Win/Linux下的Firefox，Mac OS X下版本的书签栏图标间的间距更大。可以通过修改userChrome.css调整间距

修改`userChrome.css`文件，添加：

	.bookmark-item {margin:0 !important;padding:0 !important;}

根据需要调整`margin`和`padding`的值，就可以达到所需的效果。 