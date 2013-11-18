---
layout: post
title: BeautifulSoup中的class关键字
category: tip
description: 在BeautifulSoup中，到class，需要换成class_，因为class本身是Python的关键字
---

在BeautifulSoup中，到class，需要换成class_，因为class本身是Python的关键字。

例如：

    soup = BeautifulSoup(file)
    rows = soup.find("table", class_="lista2t").findAll("tr")[1:-1]