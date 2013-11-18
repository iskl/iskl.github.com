---
layout: post
title: 编译安装fish-shell
category: tip
description: https://github.com/fish-shell/
---

    git clone https://github.com/fish-shell/fish-shell.git
    cd fish-shell
    sudo apt-get install autoconf
    sudo apt-get install libncurses5-dev libncursesw5-dev
    autoconf
    ./configure
    make
    sudo make install
    fish