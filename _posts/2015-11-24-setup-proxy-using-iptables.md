---
layout: post
title: 利用 iptables 实现端口转发代理
category: 技巧
tags: [iptables]
description: 利用 iptables 实现端口转发代理
---

将1.1.1.1:123作为代理服务器，转发往来于2.2.2.2:456的连接，操作为：

```
sudo iptables -t nat -A PREROUTING -d 1.1.1.1 -p tcp --dport 123 -j DNAT --to-destination 2.2.2.2:456
sudo iptables -t nat -A POSTROUTING -d 2.2.2.2 -p tcp --dport 456 -j SNAT --to 1.1.1.1
```

设置后，可以通过以下命令查看是否生效

```
sudo iptables -t nat –L
```