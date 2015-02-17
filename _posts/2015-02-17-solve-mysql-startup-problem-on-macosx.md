---
layout: post
title: 解决 Mac 下 mysql 启动报错
category: 技巧
tags: [MacOSX, MySQL]
description: 解决 Mac 下 mysql 启动报错
---

homebrew安装mysql后，启动方式为

```
mysql.server start
```

若出现

```
. ERROR! The server quit without updating PID file (/usr/local/var/mysql/Kailai-MacBookPro.local.pid).
```

的错误，删除`/usr/local/var/mysql`下的err文件，再重试。
