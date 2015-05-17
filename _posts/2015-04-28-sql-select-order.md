---
layout: post
title: SQL查询语句执行顺序
category: 技巧
tags: [SQL]
description: SQL查询语句执行顺序
---

感觉很重要，为什么看了那么多讲解MySQL的书都没有提到？记录下来。

	(7)     SELECT 
	(8)     DISTINCT <select_list>
	(1)     FROM <left_table>
	(3)     <join_type> JOIN <right_table>
	(2)     ON <join_condition>
	(4)     WHERE <where_condition>
	(5)     GROUP BY <group_by_list>
	(6)     HAVING <having_condition>
	(9)    ORDER BY <order_by_condition>
	(10)    LIMIT <limit_number>