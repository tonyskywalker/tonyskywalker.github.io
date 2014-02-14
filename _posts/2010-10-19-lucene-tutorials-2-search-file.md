---
layout: cn_post
title: Lucene学习2 搜索文本文件
categories: [搜索]
tags: [搜索, lucene, 查询]
---

Lucene搜索文本文件简单例子

{% highlight java %}
package com.l99.lucene.search;

import java.io.File;
import java.io.IOException;

import org.apache.lucene.analysis.standard.StandardAnalyzer;
import org.apache.lucene.document.Document;
import org.apache.lucene.queryParser.ParseException;
import org.apache.lucene.queryParser.QueryParser;
import org.apache.lucene.search.IndexSearcher;
import org.apache.lucene.search.Query;
import org.apache.lucene.search.ScoreDoc;
import org.apache.lucene.search.TopDocs;
import org.apache.lucene.store.Directory;
import org.apache.lucene.store.FSDirectory;
import org.apache.lucene.util.Version;

public class Searcher {
public static void main(String[] args) throws IllegalArgumentException,
IOException, ParseException, Exception {
if (args.length != 2) {
throw new IllegalArgumentException("Usage: java " +
Searcher.class.getName() + " <index dir> <query>");
}
String indexDir = args[0];
String q = args[1];

search(indexDir, q);
}

private static void search(String indexDir, String q)
throws IOException, ParseException, Exception {
File f = new File(indexDir);
if (!f.exists() || !f.isDirectory()) {
throw new Exception(indexDir + " does not exist or isn't a dir.");
}

Directory indexs = FSDirectory.open(f);
IndexSearcher searcher = new IndexSearcher(indexs);

QueryParser parser = new QueryParser(Version.LUCENE_30, "contents",
new StandardAnalyzer(Version.LUCENE_30));
Query query = parser.parse(q);

long start = System.currentTimeMillis();
TopDocs hits = searcher.search(query, 10);
long end = System.currentTimeMillis();

System.err.println("Found " + hits.totalHits +
" documents (in " + (end - start) +
" milliseconds) that matched query '" + q + "':");

for (ScoreDoc scoreDoc: hits.scoreDocs) {
Document doc = searcher.doc(scoreDoc.doc);
System.out.println(doc.get("fullpath"));
}

searcher.close();
}
}
{% endhighlight %}

运行参数：index/simpletxt freedom

运行结果：

{% highlight vim %}
Found 5 documents (in 47 milliseconds) that matched query 'freedom':

D:\eclipse\eclipse\workspace\Lucene\data\simpletxt\gpl1.0.txt

D:\eclipse\eclipse\workspace\Lucene\data\simpletxt\lgpl2.1.txt

D:\eclipse\eclipse\workspace\Lucene\data\simpletxt\gpl3.0.txt

D:\eclipse\eclipse\workspace\Lucene\data\simpletxt\lpgl2.0.txt

D:\eclipse\eclipse\workspace\Lucene\data\simpletxt\gpl2.0.txt
{% endhighlight %}

