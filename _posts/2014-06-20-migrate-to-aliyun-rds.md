---
layout: post
title: 阿里云 RDS 迁移笔记
category: 技巧
tags: [阿里云, MySQL]
description: 
---

第一步，先把原有数据库备份出来

<pre>
mysqldump -h localhost -u root -p discuz > /home/kailai/jp/sql.out/discuz.sql
</pre>

其中，root是用户名，discuz是数据库名，\>之后的是备份的文件名
 
第二步，在RDS的数据库管理页面上，新建相应的数据库用户名和数据库
 
第三步，在云服务器中执行

	mysql -h rdsbryqmebryqme.mysql.rds.aliyuncs.com -u discuz -p discuz

来连接上RDS

其中，`rd...`是实例名，`-u`之后的`discuz`是用户名，`-p`之后的`discuz`是数据库名

连接成功后执行

	source /home/kailai/jp/sql.out/discuz.sql

即可
 
最后，修改写在各个程序中的数据库地址等信息