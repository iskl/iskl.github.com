---
layout: post
title: 安装Ruby on Rails
category: tip
description: 安装所需包；下载安装RVM；当前环境载入RVM配置；更改gem源到淘宝；安装Ruby1.9.3；设置使用1.9.3版Ruby并将其设置为默认；在当前版本下创建gemset；设置当前gemset使用gitlabset；安装bundler和rails
---

    #安装所需包
    sudo apt-get install -y build-essential openssl curl libcurl3-dev libreadline6 libreadline6-dev git zlib1g zlib1g-dev libssl-dev libyaml-dev libxml2-dev libxslt-dev autoconf automake libtool imagemagick libmagickwand-dev libpcre3-dev libsqlite3-dev libmysql-ruby libmysqlclient-dev
    sudo apt-get install -y nodejs
    
    #下载安装RVM
    curl -L get.rvm.io | bash -s stable
    
    #当前环境载入RVM配置
    source ~/.bashrc
    source ~/.bash_profile
    
    #更改gem源到淘宝
    sed -i -e 's/ftp\.ruby-lang\.org\/pub\/ruby/ruby\.taobao\.org\/mirrors\/ruby/g' ~/.rvm/config/db
    
    #列出支持的Ruby版本
    rvm list known
    
    #安装Ruby1.9.3
    rvm install 1.9.3

    #列出所有安装的Ruby版本
    rvm list
    
    #设置使用1.9.3版Ruby并将其设置为默认
    rvm use 1.9.3 --default
    
    #在当前版本下创建gemset
    rvm gemset create gitlabset
    
    #列出所有gemset
    rvm gemset list
    
    #设置当前gemset使用gitlabset
    rvm use 1.9.3@gitlabset
    
    #安装bundler和rails
    gem install bundler rails
    
    #检测bundler和rails版本
    bundle -v
    rails -v