---
layout: cn_post
title: 2014working weibo点滴记录4 deep semantics
categories: [生活]
tags: [weibo]
---

2014-7-17

http://blog.ranjansakalley.com/2014/03/analysing-semi-structured-text-and-extracting-features.html blog.ranjansakalley.com Analysing semi-structured text and extracting features Tokenisation Building a knowledge base Blocking and labelling Building a Positional model Building a Sequencial model Inference

http://eng.kifi.com/from-word2vec-to-doc2vec-an-approach-driven-by-chinese-restaurant-process/ eng.kifi.com From word2vec to doc2vec: an approach driven by Chinese restaurant process 这里讲的挺细，有demo有code！

2014-7-19

http://www.cppblog.com/guijie/archive/2014/07/09/207585.html 中科院自动化所 Andrew Ng《Deep Learning：Overview and Trends》百度拥有大数据和强大的计算能力；有敏捷的机构，能快速地调配资源去需要的地方，也能够将技术快速落地，比如GPU的落地；同时，我被我所遇到的人所折服，比如Robin、王劲、余凯和张潼。 百度在gpu方面确实

http://lemurproject.org/ The Lemur Project develops search engines, browser toolbars, text analysis tools, and data resources that support information retrieval and text mining software. Indri search engine, Lemur Toolbar, and ClueWeb09 dataset. lemur的几个项目都很实用啊！！！

http://lemurproject.org/clueweb09.php/ http://lemurproject.org/clueweb12.php/ The ClueWeb09 and ClueWeb12 Dataset 英文的资源确实太丰富了，语料库都是TB级的，相比中文找到GB级的都很困难。
@tony的微博
O网页链接 The Lemur Project develops search engines, browser toolbars, text analysis tools, and data resources that support information retrieval and text mining software. Indri search engine, Lemur Toolbar, and ClueWeb09 dataset. lemur的几个项目都很实用啊！！！

http://boston.lti.cs.cmu.edu/clueweb12/ The number of sites selected from each country depended on its relative population size, for example, United States (71.0%), United Kindom (14.0%), Canada (7.7%), Australia (5.2%), Ireland (3.8%), and New Zealand (3.7%). 老外统计抽样很合理
@tony的微博
O网页链接 The Lemur Project develops search engines, browser toolbars, text analysis tools, and data resources that support information retrieval and text mining software. Indri search engine, Lemur Toolbar, and ClueWeb09 dataset. lemur的几个项目都很实用啊！！！

http://aws.amazon.com/cn/publicdatasets/ Common Crawl Corpus：包含超过 50 亿网页的 Web 爬取数据语料库 Google Books Ngrams：包含谷歌图书 n-gram 语料库的数据集 Freebase Data Dump：包含 Freebase 系统中当前事实和声明的数据转储 amazon aws这个数据集很强大啊！！！ 未来的云计算和存储平台确实不是吹的！！！

http://m.blog.csdn.net/blog/jj12345jj198999/27352659 同义词查找 对词先进行聚类（用word2vec自带的即可），然后进行层次聚类（更细粒度的聚类），最后就能找到意思最为接近的词对了，同义词基本都在其中。 真是写手啊，每天能写这么多文章吗？

文本聚类 对文本进行聚类时可以考虑使用词向量的特征，只需要考虑如何用词来表征文本即可，最容易想到的就是用关键词来代替文本，依据关键词聚类的结果就能够得到文本的聚类结果。关键词提取用TF-IDF，然后用word2vec训练得到关键词向量，再用k-means聚类，最后文本就能够以关键词的类别进行分类了。
@tony的微博
O网页链接 同义词查找 对词先进行聚类（用word2vec自带的即可），然后进行层次聚类（更细粒度的聚类），最后就能找到意思最为接近的词对了，同义词基本都在其中。 真是写手啊，每天能写这么多文章吗？

现在数据集越来越多了，只是中文的资源太少。 //@52nlp:默默转给大数据专家 //@tinyfool: 赞 //@韩先培: //@王斌_ICTIR:默默转给公司
@AixinSG
这个数据集够大，26亿网页， 183TB (注意是T不是G). 只有2T硬盘的表示只能转需 http://blog.commoncrawl.org/

2014-7-20

http://colah.github.io/ colah.github.io 现在把博客等小型站点放在github上的越来越多了。 Christopher Olah最近写了几篇deep nlp方面的文章，确实不错。

Understanding Convolutions - July 13, 2014 Conv Nets: A Modular Perspective - July 8, 2014 Deep Learning, NLP, and Representations - July 7, 2014 Fanfiction, Graphs, and PageRank - July 6, 2014 Neural Networks, Manifolds, and Topology - April 6, 2014
@tony的微博
O网页链接 colah.github.io 现在把博客等小型站点放在github上的越来越多了。 Christopher Olah最近写了几篇deep nlp方面的文章，确实不错。

2014-7-21

aws上做些临时的大数据处理非常好！ //@李沐M:点赞。有次老板在deadline前三小时喝了杯咖啡回头就把目标函数改了，只好冲上aws开了一大波机器跑了几百个matlab一小时把所有实验重跑了一遍。deadline前救命技能。
@grapeot
新技能get! 图中是我的128核240G内存的AWS cluster：数据和本地自动同步无需手动上传下载；所有配置可在5~10分钟内完成；成本1美元1小时，不开机不收钱；提交任务只需一行代码直观简单；自动负载均衡 详情参见https://grapeot.me/easy-and-cheap-cluster-building-on-aws.html

2014-7-22

2014-07-22 21:34:29,093 : INFO : PROGRESS: at 99.41% words, alpha 0.00074, 128771 words/s 2014-07-22 21:34:29,694 : INFO : training on 16718844 words took 129.7s, 128935 words/s

Vocab size: 71290 Words in train file: 16718843 Alpha: 0.000121 Progress: 99.58% Words/thread/sec: 39.11k 428.82user 0.34system 1:51.71elapsed 384%CPU (0avgtext+0avgdata 1017760maxresident)k 195408inputs+112704outputs (1major+66297minor)pagefaults 0swaps
@tony的微博
2014-07-22 21:34:29,093 : INFO : PROGRESS: at 99.41% words, alpha 0.00074, 128771 words/s 2014-07-22 21:34:29,694 : INFO : training on 16718844 words took 129.7s, 128935 words/s

clang-3.0 Alpha: 0.000121 Progress: 99.58% Words/thread/sec: 34.52k 485.34user 0.23system 2:04.65elapsed 389%CPU (0avgtext+0avgdata 1017680maxresident)k 0inputs+112704outputs (0major+66294minor)pagefaults 0swaps //@tony的微博:Vocab size: 71290 Words in train file: 16718843 Alpha:
@tony的微博
2014-07-22 21:34:29,093 : INFO : PROGRESS: at 99.41% words, alpha 0.00074, 128771 words/s 2014-07-22 21:34:29,694 : INFO : training on 16718844 words took 129.7s, 128935 words/s

2014-7-23

编程中good abstraction远胜那些争吵，当然如果擅长c/c++可以做更多的事情！像eigen这样的库，确实很强大！应该用好！ //@陈天奇怪:有good abstraction很好，只是matlab提供的功能相对单一而已。而整个算法往往不只是matrix operation，C++里面的library类似eigen提供了类似matlab的abstraction，可以
@余凯_西二旗民工
一篇好文章，题目“Google's Hybrid Approach to Research". 有一点建议特别想分享给有志于工业界发展的博士生们 － write production or near-production code from day one, do NOT use Matlab. http://static.googleusercontent.com/external_content/untrusted_dlcp/research.google.com/en//pubs/archive/38149.pdf

CPU E5-2620 v2 @ 2.10GHz 12Threads Alpha: 0.000121 Progress: 99.58% Words/thread/sec: 17.59k real 1m31.485s user 15m50.231s sys 0m0.271s //@tony的微博:clang-3.0 Alpha: 0.000121 Progress: 99.58% Words/thread/sec: 34.52k 485.34user 0.23system 2:04.65elapsed 389%CPU (0avgtext+0avgda
@tony的微博
2014-07-22 21:34:29,093 : INFO : PROGRESS: at 99.41% words, alpha 0.00074, 128771 words/s 2014-07-22 21:34:29,694 : INFO : training on 16718844 words took 129.7s, 128935 words/s

4Threads Alpha: 0.000049 Progress: 99.87% Words/thread/sec: 25.03k real 2m52.932s user 11m11.055s sys 0m0.261s 20Threads Alpha: 0.000166 Progress: 99.40% Words/thread/sec: 10.71k real 1m26.334s user 25m56.011s sys 0m0.319s //@tony的微博:CPU E5-2620 v2 @ 2.10GHz 12Threads Alpha: 0
@tony的微博
2014-07-22 21:34:29,093 : INFO : PROGRESS: at 99.41% words, alpha 0.00074, 128771 words/s 2014-07-22 21:34:29,694 : INFO : training on 16718844 words took 129.7s, 128935 words/s

word2vec目前很难利用多核心的优势啊，改用atlas或eigen优化下，看看效果吧！ //@tony的微博:CPU E5-2620 v2 @ 2.10GHz 12Threads Alpha: 0.000121 Progress: 99.58% Words/thread/sec: 17.59k real 1m31.485s user 15m50.231s sys 0m0.271s //@tony的微博:clang-3.0 Alpha: 0.000121 Progress: 99.58%
@tony的微博
2014-07-22 21:34:29,093 : INFO : PROGRESS: at 99.41% words, alpha 0.00074, 128771 words/s 2014-07-22 21:34:29,694 : INFO : training on 16718844 words took 129.7s, 128935 words/s

没想到jeff dean也在用eigen，不知道google内部对gotoblas、atlas或eigen的支持怎样，或者有自己的实现。 //@vinW:这里有个比较http://nghiaho.com/?p=936 opencv armadillo eigen 貌似大矩阵相乘求逆eigen有优势，svd弱点。我这种matlab深度用户，的确相信未来是matix的
@李沐M
一直在关注好的矩阵（尤其是稀疏）计算库，目前似乎没有悬念就是eigen了。因为jeff dean刚在两周前提了一个bug: http://eigen.tuxfamily.org/bz/show_bug.cgi?id=613 （据说google码农的唯一忠诚对象就是jeff）

有good abstraction很好，只是matlab提供的功能相对单一而已。而整个算法往往不只是matrix operation，C++里面的library类似eigen提供了类似matlab的abstraction，可以写出简单高效的代码。C++非常适合所有事情都DIY的人群。但是high abstraction永远是正确的选择，even in C++。赞！！！

长期写C++代码的人会注意积累，形成自己的library，有很好的abstraction. 后来开发效率越来越高。我曾经合作过的同事里，最令我欣赏的都是这样。其中有一位好朋友，从本科开始就专注于神经网络，本科时的代码，十余年后还在用，他用神经网络做几乎所有的问题，语音，图像，推荐。赞！！！
@tony的微博
有good abstraction很好，只是matlab提供的功能相对单一而已。而整个算法往往不只是matrix operation，C++里面的library类似eigen提供了类似matlab的abstraction，可以写出简单高效的代码。C++非常适合所有事情都DIY的人群。但是high abstraction永远是正确的选择，even in C++。赞！！！


