---
layout: post
title: Mount Goflex Home to Raspberry Pi
category: 技巧
tags: [Shell, NAS, RaspberryPi, GoFlexHome]
description: Mount Goflex Home to Raspberry Pi
---


	sudo mount -t cifs -o rw,soft,rsize=8192,wsize=8192,username=username,password=password "//nasip/GoFlex Home Public/" /media/Public