---
layout: cn_post
title: Lucene学习4 Tika内容提取
categories: [search]
tags: [search, lucene, tika, extraction]
---

Tika提取富文本文档简单例子

首先编译Tika，基本步骤：

1. 下载Maven3.0，解压，设置bin环境变量，“mvn -version” 命令会显示maven相关信息；

2. 下载Tika0.7，解压，进入当前目录，"mvn install" 命令会编译Tika，生成相关的jar文件等；

添加tika-app-0.7.jar到java项目编译目录。

{% highlight java %}
package com.l99.lucene.index;

import java.io.File;
import java.io.FileInputStream;
import java.io.IOException;
import java.io.InputStream;
import java.util.ArrayList;
import java.util.Collections;
import java.util.HashSet;
import java.util.Iterator;
import java.util.List;
import java.util.Set;

import org.apache.lucene.analysis.Analyzer;
import org.apache.lucene.analysis.standard.StandardAnalyzer;
import org.apache.lucene.document.Document;
import org.apache.lucene.document.Field;
import org.apache.lucene.index.IndexWriter;
import org.apache.lucene.store.Directory;
import org.apache.lucene.store.FSDirectory;
import org.apache.lucene.util.Version;
import org.apache.tika.config.TikaConfig;
import org.apache.tika.metadata.Metadata;
import org.apache.tika.parser.AutoDetectParser;
import org.apache.tika.parser.ParseContext;
import org.apache.tika.parser.Parser;
import org.apache.tika.sax.BodyContentHandler;
import org.xml.sax.ContentHandler;

public class TikaIndexer {
private static Set<String> textMetadataFields = new HashSet<String>();

static {
textMetadataFields.add(Metadata.TITLE);
textMetadataFields.add(Metadata.AUTHOR);
textMetadataFields.add(Metadata.COMMENTS);
textMetadataFields.add(Metadata.KEYWORDS);
textMetadataFields.add(Metadata.DESCRIPTION);
textMetadataFields.add(Metadata.SUBJECT);
}

public static void main(String[] args) throws Exception {
if (args.length != 2) {
throw new IllegalArgumentException("Usage: java" +
TikaIndexer.class.getName() + " <index dir> <data dir>");
}

TikaConfig config = TikaConfig.getDefaultConfig();
List<String> parsers = new ArrayList<String>(config.getParsers().keySet());

Collections.sort(parsers);
Iterator<String> itor = parsers.iterator();
System.out.println("Mime type parsers:");

while(itor.hasNext()) {
System.out.println(" " + itor.next());
}
System.out.println();

String indexDir = args[0];
String dataDir = args[1];

long start = System.currentTimeMillis();
int numIndexed = index(indexDir, dataDir);
long end = System.currentTimeMillis();

System.out.println("Indexing " + numIndexed + " files took " +
(end - start) + " milliseconds");
}

public static int index(String indexDir, String dataDir)
throws Exception {
File data = new File(dataDir);
if (!data.exists() || !data.isDirectory()) {
throw new IOException(data + " does not exist or isn't a dir");
}

Directory index = FSDirectory.open(new File(indexDir));
Analyzer analyzer = new StandardAnalyzer(Version.LUCENE_30);
IndexWriter writer = new IndexWriter(index, analyzer, true,
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
Metadata metadata = new Metadata();
metadata.set(Metadata.RESOURCE_NAME_KEY, f.getName());

InputStream stream = new FileInputStream(f);
Parser parser = new AutoDetectParser();

ContentHandler handler = new BodyContentHandler();
ParseContext context = new ParseContext();
context.set(Parser.class, parser);

try {
parser.parse(stream, handler, metadata, new ParseContext());
} finally {
stream.close();
}

Document doc = new Document();
doc.add(new Field("contents", handler.toString(),
Field.Store.YES, Field.Index.ANALYZED));

for (String name: metadata.names()) {
String value = metadata.get(name);
if (textMetadataFields.contains(name)) {
doc.add(new Field("contents", value,
Field.Store.NO, Field.Index.ANALYZED));
}
doc.add(new Field(name, value,
Field.Store.YES, Field.Index.NO));
}

doc.add(new Field("pathname", f.getCanonicalPath(),
Field.Store.YES, Field.Index.NOT_ANALYZED));
doc.add(new Field("filename", f.getName(),
Field.Store.YES, Field.Index.NOT_ANALYZED));

return doc;
}
}
{% endhighlight %}

运行参数：index/richtext data/richtext

运行结果：

{% highlight vim %}
Mime type parsers:

application/epub+zip

application/java-vm

application/mbox

application/msword

application/pdf

application/rtf

application/vnd.ms-excel

application/vnd.ms-excel.addin.macroenabled.12

application/vnd.ms-excel.sheet.binary.macroenabled.12

application/vnd.ms-excel.sheet.macroenabled.12

application/vnd.ms-excel.template.macroenabled.12

application/vnd.ms-outlook

application/vnd.ms-powerpoint

application/vnd.ms-powerpoint.addin.macroenabled.12

application/vnd.ms-powerpoint.presentation.macroenabled.12

application/vnd.ms-powerpoint.slideshow.macroenabled.12

application/vnd.ms-word.document.macroenabled.12

application/vnd.ms-word.template.macroenabled.12

application/vnd.oasis.opendocument.chart

application/vnd.oasis.opendocument.chart-template

application/vnd.oasis.opendocument.formula

application/vnd.oasis.opendocument.formula-template

application/vnd.oasis.opendocument.graphics

application/vnd.oasis.opendocument.graphics-template

application/vnd.oasis.opendocument.image

application/vnd.oasis.opendocument.image-template

application/vnd.oasis.opendocument.presentation

application/vnd.oasis.opendocument.presentation-template

application/vnd.oasis.opendocument.spreadsheet

application/vnd.oasis.opendocument.spreadsheet-template

application/vnd.oasis.opendocument.text

application/vnd.oasis.opendocument.text-master

application/vnd.oasis.opendocument.text-template

application/vnd.oasis.opendocument.text-web

application/vnd.openxmlformats-officedocument.presentationml.presentation

application/vnd.openxmlformats-officedocument.presentationml.slideshow

application/vnd.openxmlformats-officedocument.presentationml.template

application/vnd.openxmlformats-officedocument.spreadsheetml.sheet

application/vnd.openxmlformats-officedocument.spreadsheetml.template

application/vnd.openxmlformats-officedocument.wordprocessingml.document

application/vnd.openxmlformats-officedocument.wordprocessingml.template

application/vnd.sun.xml.writer

application/vnd.visio

application/vnd.wap.xhtml+xml

application/x-archive

application/x-asp

application/x-bzip

application/x-bzip2

application/x-cpio

application/x-gtar

application/x-gzip

application/x-midi

application/x-tar

application/x-tika-msoffice

application/x-tika-ooxml

application/x-vnd.oasis.opendocument.chart

application/x-vnd.oasis.opendocument.chart-template

application/x-vnd.oasis.opendocument.formula

application/x-vnd.oasis.opendocument.formula-template

application/x-vnd.oasis.opendocument.graphics

application/x-vnd.oasis.opendocument.graphics-template

application/x-vnd.oasis.opendocument.image

application/x-vnd.oasis.opendocument.image-template

application/x-vnd.oasis.opendocument.presentation

application/x-vnd.oasis.opendocument.presentation-template

application/x-vnd.oasis.opendocument.spreadsheet

application/x-vnd.oasis.opendocument.spreadsheet-template

application/x-vnd.oasis.opendocument.text

application/x-vnd.oasis.opendocument.text-master

application/x-vnd.oasis.opendocument.text-template

application/x-vnd.oasis.opendocument.text-web

application/xhtml+xml

application/xml

application/zip

audio/basic

audio/midi

audio/mpeg

audio/x-aiff

audio/x-wav

image/bmp

image/gif

image/jpeg

image/png

image/svg+xml

image/tiff

image/vnd.wap.wbmp

image/x-icon

image/x-psd

image/x-xcf

text/html

text/plain

video/x-flv

Indexing D:\eclipse\eclipse\workspace\Lucene\data\richtext\addressbook-entry.xml

Indexing D:\eclipse\eclipse\workspace\Lucene\data\richtext\addressbook.xml

Indexing D:\eclipse\eclipse\workspace\Lucene\data\richtext\HTML.html

Indexing D:\eclipse\eclipse\workspace\Lucene\data\richtext\MSWord.doc

Indexing D:\eclipse\eclipse\workspace\Lucene\data\richtext\MSWordXML.docx

Indexing D:\eclipse\eclipse\workspace\Lucene\data\richtext\PDF.pdf

log4j:WARN No appenders could be found for logger (org.apache.pdfbox.util.PDFStreamEngine).

log4j:WARN Please initialize the log4j system properly.

Indexing D:\eclipse\eclipse\workspace\Lucene\data\richtext\PlainText.txt

Indexing D:\eclipse\eclipse\workspace\Lucene\data\richtext\RTF.rtf

Indexing 8 files took 4811 milliseconds
{% endhighlight %}

