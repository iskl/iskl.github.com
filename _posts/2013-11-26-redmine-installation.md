---
layout: post
title: Redmine 安装笔记
category: 技巧
tags: [Redmine, Ruby, rvm]
description: Redmine 安装笔记
---

## 安装RVM：

	curl -L get.rvm.io | bash -s stable

退出fish和screen

	source /home/kailai/.rvm/scripts/rvm
	rvm requirements
 
## 安装Ruby：

	rvm install 1.9.3-p392
	rvm use 1.9.3-p392
	rvm gemset create redmine233
	rvm use 1.9.3-p392@redmine233
 
## 配置Redmine数据库：

	mysql -u root -p
	> CREATE DATABASE redmine CHARACTER SET utf8;
	> CREATE USER 'redmine'@'localhost' IDENTIFIED BY 'my_password';
	> GRANT ALL PRIVILEGES ON redmine.* TO 'redmine'@'localhost';
 
## 安装Redmine：

	wget http://rubyforge.org/frs/download.php/77023/redmine-2.3.2.tar.gz
	tar -xzvf redmine-2.3.2.tar.gz

cd到目录

	bundle install --without development test postgresql sqlite
	mkdir public/plugin_assets
	sudo chmod 777 files log tmp public/plugin_assets config.ru
 
## 配置Redmine参数：

	cp config/database.yml.example config/database.yml
	nano config/database.yml

配置production就可以了
 
## 测试：

在redmine目录

	rake generate_secret_token
	RAILS_ENV=production rake db:migrate
	RAILS_ENV=production rake redmine:load_default_data

若执行

	ruby script/rails server webrick -e production

后，在ooxx:3000访问成功，说明安装成功
 
## 安装Passenger：

	gem install passenger --no-rdoc --no-ri
	rvmsudo passenger-install-apache2-module

按提示完成

	cd /etc/apache2/mods-available

接上一步提示完成custom_passenger.conf和custom_passenger.load的创建

	sudo a2enmod custom_passenger

在mods-enabed文件夹中查看是否启用
 
## 配置Apache:

在/var/www目录下建立软链接，然后


	<VirtualHost *:80>
	    ...
	    RailsBaseURI /redmine
	    <Directory /yourpath/redmine/public>
	            # This relaxes Apache security settings.
	            AllowOverride all
	            # MultiViews must be turned off.
	            Options -MultiViews
	    </Directory>
	    ...
	</VirtualHost>