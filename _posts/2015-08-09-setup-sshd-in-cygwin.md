---
layout: post
title: Cygwin 下架设 ssh-server 的若干问题
category: 技巧
tags: [Cygwin, sshd]
description: Cygwin 下架设 ssh-server 的若干问题
---

Cygwin下开启sshd不像Debian下开箱即用，问题一堆，逐个解决，记录之。


配置sshd：

```
ssh-host-config
```

若出现`Cannot find required command /usr/bin/getent`，用pact安装getent

若出现`The permissions on the directory /var are not correct.`，将/var的访问权限设为755

两个选项：

```
Should StrictModes be used? (yes/no) yes
Should privilege separation be used? (yes/no) no
```

完成后，`net start sshd`启动后台服务。

若失败，从`/var/log/sshd.log`中找错误信息

若错误信息中出现`Could not load host key: /etc/ssh_host_ooxx_ooxx`，多半是权限问题，通过以下命令设置正确权限

```
chown cyg_server /etc/ssh*
chmod 600 /etc/ssh*
```
