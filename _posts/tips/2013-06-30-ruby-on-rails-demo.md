---
layout: post
title: Ruby on Rails demo
category: tip
---

    rails new demo

长时间显示"run bundle install"，可能是[下载gem时撞墙所致](http://ruby-china.org/topics/914 "run bundle install 卡住很久")，Ctrl+C跳出，做如下修改

    cd demo
    nano Gemfile

修改source为http://ruby.taobao.org

    bundle install
    rails server

通过http://127.0.0.1:3000访问