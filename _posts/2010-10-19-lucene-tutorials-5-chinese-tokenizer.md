---
layout: cn_post
title: Lucene学习5 中文分词
categories: [search]
tags: [search, lucene, tokenizer]
---

Lucene一般使用StandardAnalyzer，对于中文采用单字分词方法，效果不是很好。

Lucene的contrib里有三个相关的中文分析器，CJKAnalyzer， ChineseAnalyzer和SmartChineseAnalyzer。其中CJKAnalyzer主要是双字分词，ChineseAnalyzer主要是单字分词，而SmartChineseAnalyzer使用语法分析和概率模型效果最好。

将学习1中StandardAnalyzer换成SmartChineseAnalyzer，添加lucene-smartcn-3.0.2.jar.

我从百度百科上copy一些编程语言的内容，用记事本保存。结果我的windows7 64enterprise（en）记事本没法保存中文，本来想转换成word文件，结果用wps打开也是乱码，只好重新copy。

运行参数：index/cntext data/cntext

运行结果：

{% highlight vim %}
Indexing D:\eclipse\eclipse\workspace\Lucene\data\cntext\erlang.doc

Indexing D:\eclipse\eclipse\workspace\Lucene\data\cntext\erlang.txt

Indexing D:\eclipse\eclipse\workspace\Lucene\data\cntext\haskell.doc

Indexing D:\eclipse\eclipse\workspace\Lucene\data\cntext\haskell.txt

Indexing D:\eclipse\eclipse\workspace\Lucene\data\cntext\java.doc

Indexing D:\eclipse\eclipse\workspace\Lucene\data\cntext\java.txt

Indexing D:\eclipse\eclipse\workspace\Lucene\data\cntext\ocaml.doc

Indexing D:\eclipse\eclipse\workspace\Lucene\data\cntext\ocaml.txt

Indexing D:\eclipse\eclipse\workspace\Lucene\data\cntext\prolog.doc

Indexing D:\eclipse\eclipse\workspace\Lucene\data\cntext\prolog.txt

Indexing D:\eclipse\eclipse\workspace\Lucene\data\cntext\python.doc

Indexing D:\eclipse\eclipse\workspace\Lucene\data\cntext\python.txt

Indexing D:\eclipse\eclipse\workspace\Lucene\data\cntext\ruby.doc

Indexing D:\eclipse\eclipse\workspace\Lucene\data\cntext\ruby.txt

Indexing D:\eclipse\eclipse\workspace\Lucene\data\cntext\scheme.doc

Indexing D:\eclipse\eclipse\workspace\Lucene\data\cntext\scheme.txt

Indexing 16 files took 3668 milliseconds
{% endhighlight %}

执行搜索，运行参数：index/cntext 编程

结果eclipse好像不支持中文，出现错误：

{% highlight vim %}
Exception in thread "main"

at org.apache.lucene.queryParser.QueryParser.parse(

at com.l99.lucene.search.Searcher.search(

at com.l99.lucene.search.Searcher.main(

Caused by:

at org.apache.lucene.queryParser.QueryParser.getWildcardQuery(

at org.apache.lucene.queryParser.QueryParser.Term(

at org.apache.lucene.queryParser.QueryParser.Clause(

at org.apache.lucene.queryParser.QueryParser.Query(

at org.apache.lucene.queryParser.QueryParser.TopLevelQuery(

at org.apache.lucene.queryParser.QueryParser.parse(

... 2 more
{% endhighlight %}

哎，中文编程真是麻烦!

org.apache.lucene.queryParser.ParseException: Cannot parse '??': '*' or '?' not allowed as first character in WildcardQueryQueryParser.java:187)Searcher.java:44)Searcher.java:29)org.apache.lucene.queryParser.ParseException: '*' or '?' not allowed as first character in WildcardQueryQueryParser.java:923)QueryParser.java:1347)QueryParser.java:1250)QueryParser.java:1178)QueryParser.java:1167)QueryParser.java:182) 

