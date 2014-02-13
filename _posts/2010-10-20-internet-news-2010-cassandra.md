---
layout: cn_post
title: Cassandra追忆 Twitter停用Cassandra的误解
categories: [system]
tags: [system, cassandra]
---

刚刚写了关于Hadoop和MongoDB的两篇文章，突然想起上个月看到Cassandra的消息。

刚辞职研究Hadoop时，看到Twitter和Digg，Reddit开始从MySQL转到Cassandra，确实激动得不得了。可是后来Twitter据说又回滚到MySQL，而Digg改版后也遇到了Cassandra的问题，一路彷徨。上个月终于看到Twitter的具体消息，文中写道：

“Twitter在博客中表示，将不再使用Cassandra数据库系统来存储Twitter信息，但却会使用该数据库来开发Twitter实时分析产品。”

“而Twitter的工程师瑞恩·金(Ryan King)在博客中直接说到：“公司的分析团队、运营团队以及基础建设团队正在使用Cassandra系统合作研发一款供Twitter后台以及客户共同使用的大规模实时数据分析产品。””

“瑞恩·金表示未来Cassandra仍将做为Twitter众多新产和服务的核心架构，包括地理定位数据库、对话题趋势的数据挖掘以及上文提到的实时分析产品。他说：“我们现在每天都在利用Cassandra来处理相关问题，它将注定陪伴我们很长时间，未来我们对于它的使用只会不断增加。””

现在我一直关注的几个NOSQL产品（Hadoop，MongoDB，Cassandra，Membase，CouchDB）都已经得到了很好的应用，未来一片光明！


