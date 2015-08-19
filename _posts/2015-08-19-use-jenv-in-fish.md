---
layout: post
title: fish 下使用 jenv
category: 技巧
tags: [fish, jenv]
description: fish 下使用 jenv
---

jenv是在shell中切换Java版本的命令行工具，在2014-03-22技巧中提到了bash下使用方法。
但是jenv对fish-shell的支持并不好。配置方法如下。

```
brew upgrade fish //2.2的fish自带export函数，jenv需要
brew install jenv
```

添加 `set PATH ~/.jenv/bin $PATH` 到 `~/.conf/fish/config.sh`

```
cd ~/.conf/fish
mkdir functions
cd functions
wget https://raw.githubusercontent.com/gcuisinier/jenv/master/fish/jenv.fish
```

重启fish-shell

```
functions //检查jenv是否在函数列表中
jenv add /path/to/java1.6/home
jenv add /path/to/java1.7/home
jenv add /path/to/java1.8/home
jenv versions //查看所有版本
jenv global 1.6
java -version //1.6
jenv global 1.7
java -version //1.7
jenv global 1.8
java -version //1.8
```