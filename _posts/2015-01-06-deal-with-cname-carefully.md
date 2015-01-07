---
layout: post
title: 慎用 CNAME 设置域名 "@" 项
category: 技巧
tags: [域名]
description: 慎用 CNAME 设置域名 "@" 项
---

如果根域名绑定了邮箱服务器（即将"@"的MX记录指向了邮件服务器），这时候在根域名上设置一个CNAME类型的记录（即将"@"的CNAME记录指向另一个域名），会导致原有MX记录被覆盖，外部发往域名邮箱的邮件无法收到。

原因可参考 [Stackoverflow - Do CNAME records also forward MX requests?](http://stackoverflow.com/questions/12204360/do-cname-records-also-forward-mx-requests)