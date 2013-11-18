---
layout: post
title: source和sh的区别
category: tip
description: When you call sh you initiate a fork (sub-process) that run a new session of /bin/sh which is probabely an symbolic link to bash. In this case, environment variables setteds by the sub-script would be dropped when the sub-script finish.
---

When you call source (or his alias .) you insert the script in the current bash process. So you could read variables setteds by the script.
When you call sh you initiate a fork (sub-process) that run a new session of /bin/sh which is probabely an symbolic link to bash. In this case, environment variables setteds by the sub-script would be dropped when the sub-script finish.