---
layout: post
title: Vagrant 部署数据库
category: 技巧
tags: [Vagrant, MySQL, MacOSX]
description: Vagrant 部署 MySQL
---

内存大的好处是可以开好多个虚拟机，让宿主机保持保持干净整洁。

## Vagrant部署虚拟机

	mkdir MySQL
	cd MySQL
	vagrant init ubuntu/trusty64

修改`Vagrantfile`，增加

	config.vm.network :forwarded_port, guest: 22, host: 20022
	config.vm.network :forwarded_port, guest: 80, host: 20080
	config.vm.network :forwarded_port, guest: 3306, host: 23306

到配置段

## 安装、配置MySQL

	vagrant up
	vagrant ssh
	sudo tasksel

在tasksel里安装LAMP，并设置数据库root密码。

接下来编辑`/etc/mysql/my.cnf`，将

	bind-address          = 127.0.0.1

注释掉，以允许外部IP连入。

	mysql -uroot -p
	GRANT ALL PRIVILEGES ON *.* TO 'root'@'%' IDENTIFIED BY 'my77r55r00tpw' WITH GRANT OPTION;

上面两句是在MySQL里给root用户外部连入的授权。

	sudo service mysql stop
	sudo service mysql start

重启服务使生效。

## 使用

在宿主机Navicat里，用root用户连`localhost:23306`，开始使用。



