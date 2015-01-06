---
layout: post
title: 利用 Dnspod API 实现 DDNS 功能
category: 技巧
tags: [Dnspod, DDNS]
description: 用 Dnspod 的 API 实现 DDNS 功能
---

在cron中添加一个定时任务，执行脚本内容如下

	curl -X POST https://dnsapi.cn/Record.Ddns -d 'login_email=EMAIL&login_password=PASSWORD&format=json&domain_id=DOMAINID&record_id=RECORDID&record_line=默认' >> /home/pi/log/ddns.log ; echo "" >> /home/pi/log/ddns.log

其中，`EMAIL`和`PASSWORD`是用户名和密码，`DOMAINID`和`RECORDID`是此域名在Dnspod中的域名ID和子域名ID，`/home/pi/log/ddns.log`是自己设置的log文件。