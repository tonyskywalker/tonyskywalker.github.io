---
layout: cn_post
title: Solr学习1 模式设计
categories: [search]
tags: [search, solr, schema]
---

Lucene只是一个信息检索库，提供了核心的索引和搜索功能，但是一个完整的搜索产品还需要很多。

Solr是在Lucene的基础上开发的，是一个完整的企业级搜索服务器，提供了强大的本地爬虫，文本提取，
搜索客户端接口，管理界面等高级功能，通过LucidImagination的推广，目前在很多互联网公司中使用.
Twitter目前已经将搜索技术从Summize转到Lucene，基于Lucene的搜索技术包括Solr，Nutch等前景可观。

Solr的模式设计。

