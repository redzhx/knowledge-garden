---
tags: 
aliases: 
title: bibliometrix
date created: 2023-01-09
date modified: 2023-01-09
---

# bibliometrix



install.packages("bibliometrix")    ##安装

library（bibliometrix）  ##加载命令

biblioshiny()            ##会打开一个借助R运行的网页，在网页中的功能项下设置参数

## 答疑解惑


[Bibliometrix - 常见问题解答](https://www.bibliometrix.org/home/index.php/faq) #[[Highlights]]

## 衡量国家维度用通讯作者的国家更准确

1）Country Scientific Production衡量“作者所在国家/地区的出场次数”。
这意味着如果一篇文章中有三位作者分别在美国、西班牙和意大利工作，那么这三个国家/地区的出现次数计数器将增加 1。换句话说，每篇文章都归因于其所有国家/地区共同作者，因此将被计算为作者的次数（在上面的示例中，三次）。
因此，生产指标的总和必然超过文章总数（至少如果所有文章都是单签名的）。

2)有一个与国家维度相关的替代分析，也在 biblioshiny 中提出，称为“通讯作者的国家”，其中每篇文章根据通讯作者的从属关系与一个国家相关联。
在这种情况下，每个国家/地区的频率对应于文章总数。
此外，该分析还计算了至少有一位作者与通讯作者所在国家/地区以外的国家有隶属关系的文章的比例。
索引称为多国出版物 (MCP)。

## Analysis of Cited References 
引用最多的参考文献或引用最多的第一作者（参考文献）的频次。

对于每篇手稿，引用的参考文献都在一个字符串中，存储在数据框的“CR”列中。

为了正确提取，您需要识别 ISI 或 SCOPUS 数据库使用的不同参考文献之间的分隔符字段。通常，默认分隔符是“;” 或`". "`（带双空格的点）。

## 作者 h 指数

h 指数是一种作者级别的指标，衡量科学家或学者出版物的生产力和引文影响。

该索引基于科学家被引用次数最多的论文集以及他们在其他出版物中收到的引用次数。


### 使用参考
- 官网FAQ: [Site Unreachable](https://www.bibliometrix.org/home/index.php/faq)
- [A brief introduction to bibliometrix](http://www.bibliometrix.org/vignettes/Introduction_to_bibliometrix.html)
- colordi. 用Bibiometrix进行文献计量分析. 知乎专栏. Published 2021. Accessed January 9, 2023. https://zhuanlan.zhihu.com/p/425515491
- 作者：荫荫佳木 https://www.bilibili.com/read/cv18297389 出处：bilibili
- [Redirecting](https://linkinghub.elsevier.com/retrieve/pii/S0148296321003155)

# 相关

解决Bibliometrix 使用中无法Clustering分析报错问题。

## 操作步骤： 

1.重装最新版Rstudio
( [Rstudio官网](https://posit.co/)，[RSTUDIO-2022.12.0-353.DMG](https://download1.rstudio.org/electron/macos/RStudio-2022.12.0-353.dmg))

2.重新安装Bibliometrix  
参考官网说明：https://www.bibliometrix.org/vignettes/Introduction_to_bibliometrix.html
控制界面输入安装Bibliometrix包代码 install.packages('bibliometrix',dependencies = TRUE)
显示程序安装了dependency ”openalexR"
![image.png](https://xxpic.oss-cn-qingdao.aliyuncs.com/pic/20230206193812.png)

3.重新运行Bibliometrix。Clustering成功运行。 

额外发现： 版本更新了。 新版本速度更快， 更稳定。 

## 出错原因分析：  
刚开始学信息分析时， 自己先搜索教程先安装好了R Studio和Bibliometrix， 当时教程里使用的代码是： install.packages("bibliometrix") 缺失dependencies。导致程序运行出错。 
经验教训： 一定要看官网指引。 不然掉进坑里太浪费时间了。 

