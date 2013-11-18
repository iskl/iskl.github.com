---
layout: post
title: dpkg命令众参数
category: tip
description: 安装；卸载；完全卸载包括配置；查看状态
---

安装

    sudo dpkg -i rpimonitor_2.0-1_all.deb #文件名

卸载

    sudo dpkg -r rpimonitor #不是文件名是包名

完全卸载包括配置

    sudo dpkg -P rpimonitor #不是文件名是包名

查看状态

    dpkg -l | grep "rpimonitor"
    #"ii"表示"installed ok installed"
    #"rc"表示"removed ok config-files"，配置文件还在
    #没有返回表示完全卸载