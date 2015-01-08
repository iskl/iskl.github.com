---
layout: post
title: 禁止 / 解禁 Linux 中的 ping 功能
category: 技巧
tags: [ping, Linux, TCP/IP]
description: 禁止 / 解禁 Linux 中的 ping 功能
---

	sudo vim /proc/sys/net/ipv4/icmp_echo_ignore_all

将值改为1，为禁止PING
将值改为0，为解除禁止PING