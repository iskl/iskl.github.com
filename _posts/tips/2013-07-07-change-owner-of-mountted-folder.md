---
layout: post
title: 改变mount目录的用户权限
category: tip
description: sudo chown -R pi:pi /mnt
---

一般通过简单地mount，即`sudo mount /dev/sda1 /mnt`所得到的目录都是root拥有的，普通用户操作需带sudo提权。

可以通过

     sudo chown -R pi:pi /mnt

更改目录权限到制定用户完成所属权修改。