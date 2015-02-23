---
layout: cn_post
title: 2014reading weibo信息轨迹5 language
categories: [生活]
tags: [weibo]
---

2014-5-12

dan klein的博士论文: word的context延展至全文，且不考虑词的位置（bow)就变成了topic model之类，more semantic，当context很小且考虑位置就是distributional clustering，more syntax

大体上是这样，几个决定性的component, 1）windows的大小（5-words，句子, 文章, decay with distance），2)是否考虑语序， 3)词之间interaction的方式（linear/nonlinear, coherence/prediction, error function）。word embedding！

词聚类：词义相似度可以分为两个角度来看：横向组合(syntagmatical) 和纵向聚合(paradigmatical)相似性。从语义分析来看，后者更为有用。经典的Brown聚类更倾向计算横向组合相似性。word2vec是计算纵向聚合相似性。 word embedding！

以色列经济部5日宣布，Intel已向以色列政府递交计划，Intel将投资58亿美元升级改造它在以色列南部的22nm芯片工厂，用于生产全新的10nm芯片，这种芯片将被用于可穿戴式智能设备、物联网组件等产品中，以色列政府将为该项目提供10亿美元补助。

2 长尾数据方面。LDA这些主题模型，隐含了一个指数分布假设，低频词没多大贡献，所以词的聚类去重后只有几百几千。从逻辑的角度，我是这么理解的：模型model的分布不均衡，表达式(也就是词)频率不是模型的频率。过滤掉的不应该是低频词而是低频模型。word2vec有点这个意思了。by 西瓜

http://book.55www.com/jingyong/index.htm 55www 金庸小说 在线文本

http://www.oklink.net/wxsj/jing-yong/sky-dragon/001.htm oklink 白鹿书院 金庸武侠 在线文本

http://www.my285.com/wuxia/jinyong/tlbb/001.htm my285 梦远书城 金庸武侠 在线文本

http://www.cadal.zju.edu.cn/search/bookSearch cadal 很多在线图书，浙大作品 可惜需要注册借阅。

http://www.txthj.com/post/category/wuxia txthj 武侠文本合集下载

http://club.topsage.com/thread-2472913-1-1.html topsage 大家论坛 大量图书资源下载

版权是个大问题，不知道那些网站的数据靠谱些，服务稳定，可以作为在线数据源。

http://club.topsage.com/forum-468-1.html topsage 大家论坛，英文的资料很全

http://bbs.dxsxs.com/thread-128-1-1.html dxsxs 大学生小说网 不少 武侠文本资源

http://www.dxsxs.com/book/html/4.html dxsxs 大学生小说网 金庸文本 可惜质量都差不多。

http://www.jinyongbbs.com/jinyong/tlbb/ jinyongbbs 金庸在线文本

http://www.gulongbbs.com/jinyong/ gulongbbs 金庸在线文本

http://www.400gb.com/shared/folder_3013525_3c172688/ ctdisk 金庸繁体 pdf版

http://www.400gb.com/shared/folder_2967035_1be721c9/ 400gb 金庸大量资源汇总

中文的东西各方面都很费劲啊

移动应用「杏树林医学文献」获得美国VC几十万美元天使投资，垂直于医生领域为他们提供最新资讯。这个不错。

http://bib.oxfordjournals.org/content/current oxfordjournals 医学paper

http://bd2k.nih.gov/index.html#sthash.YPW6wLnv.dpbs NIH Big Data to Knowledge (BD2K)

http://ivory.idyll.org/blog//2014-assembling-soil.html 借助生物医学，打开另一扇门，那一直没有时间去做的未来。

http://ivory.idyll.org/blog//2014-moore-ddd-round2.html ivory.idyll.org 生物医学，也很有意思。

Titus的基于Khmer的Digital Normalization, Partitioning , Assembly策略的土壤元基因组数据分析的文章发表在了PNAS上，http://www.pnas.org/content/111/13/4904.abstract 上一篇介绍基于Bloom Filters的Normalization策略的文章也是在PNAS上。http://www.pnas.org/content/109/33/13272.abstract 。 pnas.org 很不错。

http://blog.mlin.net/2014/03/blogging-my-genome-episode-1-parting.html http://blog.mlin.net/2014/03/blogging-my-genome-episode-2-scratching.html http://blog.mlin.net/2014/03/blogging-my-genome-episode-3-data.html blog.mlin.net 生物医学方面的researcher and engineer 也有不少open infos。

http://gossipcoder.com/?p=1335 gossipcoder.com 生命科学中的大数据 认识 陈钢 源于《统计思维》，然后对华大基因有了不一样的认识。

http://blog.fejes.ca/?p=2418 blog.fejes.ca What is a bioinformatician

#NGS知识库# Sequence Ontology（序列本体论， http://www.sequenceontology.org/）， Variation Ontology（变异本体论， http://variationontology.org/index.shtml） 以及变异本体论的文章刚刚在 Genome Research 出版，http://genome.cshlp.org/content/early/2013/10/25/gr.157495.113.abstract 。 VariO 在DNA，RNA，以及Protein 三个水平对变异进行描述。强大！

生物男的春天要来了吗：据CrunchBase和TechCrunch最新数据显示，上个月全美初创企业共获得约40亿美元的投资，其中BioTech类获得最多，约有7.8亿；电商次之，4.8亿；软件业，4亿，硬件业，3亿。SF湾区初创企业获得了全美四分之一的投资，超过LA、Boston、NY的总和。

大数据给生物医学带来一个很好的机遇，没想到这么快就到了。

2014-5-13

http://davetang.org/muse/2014/04/03/bioinformatics-data-skills/ davetang.org Reading the early release of "Bioinformatics Data Skills"

UC Irvine 计算机和生物信息学教授，Pierre Baldi，合著Bioinformatics引用上千次。这里要说的是他的另一本著作，The Shattered Self: The End of Natural Evolution。听名字就比较玄，生物信息学和计算机科学结合讨论进化，从DNA、试管婴儿和克隆，到人工智能、人工生命和脑。

http://www.biomedcentral.com/bmcbioinformatics/supplements/13/S19 biomedcentral.com open access

http://www.biomedcentral.com/bmcbioinformatics/archive biomedcentral.com 大量论文资源汇总

2014-5-14

我们已经在模式识别、NLP、DL等方面做了不少乱七八糟的事，还搭了一个16*Tesla*4（不是那部电动车好嘛）的计算集群随便你调戏！ 这个很吸引人！！！

我们备好了跑步机、桌面篮球 、ASICS、Picooc、Bose&Zeppelin，你每天不累个汗出如浆我们都不会让你停！ 什么？你还在考虑能不能补充上营养？拜托，这里是饮料随便喝（碳酸类的限制）、水果随便吃（榴莲不许）、零食随便嚼、早餐都供应到酸奶了好不好！ 对脑力消耗很大的工作来说，这个很给力！！！

http://www.biostatistic.net/portal.php biostatistic.net 生物统计方面很多的信息

http://www.hindawi.com/journals/bmri/2014/240403/ hindawi.com Evaluating Word Representation Features in Biomedical Named Entity Recognition Tasks

http://www.nltk.org/book/ch07.html nltk 大量工具整合，Extracting Information from Text。



