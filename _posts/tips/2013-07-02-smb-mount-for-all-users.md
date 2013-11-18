---
layout: post
title: 所有用户均有权限访问的smb mount
category: tip
description: 在mount一个smb目录时，umask选项不可用，此时其功能由file_mode和dir_mode实现
---

在mount一个smb目录时，umask选项不可用，此时其功能由file_mode和dir_mode实现

    sudo mount -t cifs -o rw,soft,rsize=8192,wsize=8192,username=username,password=password,file_mode=0777,dir_mode=0777 "//nasip/GoFlex Home Public/" /media/Public