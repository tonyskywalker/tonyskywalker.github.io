---
layout: post
title: Lucene学习1 索引文本文件
categories: [search]
tags: [search, lucene, index]
---

Lucene 索引文本文件的简单例子：

{% highlight objc linenos %}
package com.l99.lucene.index;

import java.io.File;
import java.io.FileFilter;
import java.io.FileReader;
import java.io.IOException;

import org.apache.lucene.analysis.standard.StandardAnalyzer;
import org.apache.lucene.document.Document;
import org.apache.lucene.document.Field;
import org.apache.lucene.index.IndexWriter;
import org.apache.lucene.store.Directory;
import org.apache.lucene.store.FSDirectory;
import org.apache.lucene.util.Version;

public class Indexer {
public static void main(String[] args) throws Exception {
if (args.length != 2) {
throw new IllegalArgumentException("Usage: java" +
Indexer.class.getName() + " <index dir> <data dir>");
}
String indexDir = args[0];
String dataDir = args[1];

long start = System.currentTimeMillis();
int numIndexed = index(indexDir, dataDir, new TextFilesFilter());
long end = System.currentTimeMillis();

System.out.println("Indexing " + numIndexed + " files took " +
(end - start) + " milliseconds");
}

public static int index(String indexDir, String dataDir, FileFilter filter)
throws Exception {
File data = new File(dataDir);
if (!data.exists() || !data.isDirectory()) {
throw new IOException(data + " does not exist or isn't a dir.");
}

Directory index = FSDirectory.open(new File(indexDir));
IndexWriter writer = new IndexWriter(index,
new StandardAnalyzer(Version.LUCENE_30), true,
IndexWriter.MaxFieldLength.UNLIMITED);

indexDirectory(writer, data);
writer.optimize();
writer.close();

return writer.numDocs();
}

private static void indexDirectory(IndexWriter writer, File data)
throws IOException, Exception {
File[] datas = data.listFiles();

for (File f: datas) {
if (f.isDirectory()) {
indexDirectory(writer, f);
} else {
indexFile(writer, f);
}
}
}

private static void indexFile(IndexWriter writer, File f)
throws IOException, Exception {
if (f.isHidden() || !f.exists() || !f.canRead()) {
return;
}

System.out.println("Indexing " + f.getCanonicalPath());
Document doc = getDocument(f);
writer.addDocument(doc);
}

private static Document getDocument(File f) throws Exception {
Document doc = new Document();

doc.add(new Field("fullpath", f.getCanonicalPath(),
Field.Store.YES, Field.Index.NOT_ANALYZED));
doc.add(new Field("filename", f.getName(),
Field.Store.YES, Field.Index.NOT_ANALYZED));
doc.add(new Field("contents", new FileReader(f)));

return doc;
}

private static class TextFilesFilter implements FileFilter {
public boolean accept(File f) {
return f.getName().toLowerCase().endsWith(".txt");
}
}
}
{% endhighlight %}

运行参数: index/simpletxt data/simpletxt

运行结果:

Indexing D:\eclipse\eclipse\workspace\Lucene\data\simpletxt\apache1.0.txt

Indexing D:\eclipse\eclipse\workspace\Lucene\data\simpletxt\apache1.1.txt

Indexing D:\eclipse\eclipse\workspace\Lucene\data\simpletxt\apache2.0.txt

Indexing D:\eclipse\eclipse\workspace\Lucene\data\simpletxt\cpl1.0.txt

Indexing D:\eclipse\eclipse\workspace\Lucene\data\simpletxt\epl1.0.txt

Indexing D:\eclipse\eclipse\workspace\Lucene\data\simpletxt\freebsd.txt

Indexing D:\eclipse\eclipse\workspace\Lucene\data\simpletxt\gpl1.0.txt

Indexing D:\eclipse\eclipse\workspace\Lucene\data\simpletxt\gpl2.0.txt

Indexing D:\eclipse\eclipse\workspace\Lucene\data\simpletxt\gpl3.0.txt

Indexing D:\eclipse\eclipse\workspace\Lucene\data\simpletxt\lgpl2.1.txt

Indexing D:\eclipse\eclipse\workspace\Lucene\data\simpletxt\lgpl3.txt

Indexing D:\eclipse\eclipse\workspace\Lucene\data\simpletxt\lpgl2.0.txt

Indexing D:\eclipse\eclipse\workspace\Lucene\data\simpletxt\mit.txt

Indexing D:\eclipse\eclipse\workspace\Lucene\data\simpletxt\mozilla1.1.txt

Indexing D:\eclipse\eclipse\workspace\Lucene\data\simpletxt\mozilla_eula_firefox3.txt

Indexing D:\eclipse\eclipse\workspace\Lucene\data\simpletxt\mozilla_eula_thunderbird2.txt

Indexing 16 files took 718 milliseconds

生成索引文件：

_0.cfs

_0.cfx

segments.gen

segments_2

如果采用多文件索引格式存储，增加以下语句：

writer.setUseCompundFile(false);

运行结果，时间慢一些：

Indexing 16 files took 1232 milliseconds

生成索引文件：

_1.fdt

_1.fdx

_1.fnm

_1.frq

_1.nrm

_1.prx

_1.tii

_1.tis

segments.gen

segments_3

