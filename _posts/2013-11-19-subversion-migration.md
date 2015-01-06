---
layout: post
title: SVN 迁移笔记
category: 技巧
tags: [SVN]
description: SVN 迁移
---

执行

	sudo svnadmin dump repo位置 > myrepos.dump

备份源数据，注意`repo位置`无`/`结束

执行

	sudo svnadmin load /home/svn/myrepos < myrepos.dump
	sudo chown -R www-data:subversion myrepos

在新位置展开备份数据