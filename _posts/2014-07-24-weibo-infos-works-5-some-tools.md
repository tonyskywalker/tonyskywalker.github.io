---
layout: cn_post
title: 2014working weibo点滴记录5 some tools
categories: [生活]
tags: [weibo]
---

2014-7-24

如果能用“Distributed Representations of Sentences and Documents”写个paragraph2vec，那简直太棒了。deep semantics方面非常需要啊！
@nerdylinius
dcnn-nlp已完成大部分工作，打算再参考“Distributed Representations of Sentences and Documents”写个paragraph2vec的toolkit，到时候一起发布

2014-7-25

python确实适合做full stack engineer，尤其是做ml和nlp相关的应用，c/c++和python/shell组合非常强大。 //@52nlp:非常感谢，已更新到文本处理那块儿，看起来很不错，文档也很详细，回头试用一下 //@大山坡的春: 我们组同事之前发布了xTAS，也是基于python的text mining工具包，欢迎使用，链接： http:
@52nlp
“Python 网页爬虫 & 文本处理 & 科学计算 & 机器学习 & 数据挖掘兵器谱”，整理了一批开源的Python工具包，前面大部分都是我用过和接触过的，后面的一批来源于其他同学的线索，也欢迎大家补充 http://www.52nlp.cn/python-%E7%BD%91%E9%A1%B5%E7%88%AC%E8%99%AB-%E6%96%87%E6%9C%AC%E5%A4%84%E7%90%86-%E7%A7%91%E5%AD%A6%E8%AE%A1%E7%AE%97-%E6%9C%BA%E5%99%A8%E5%AD%A6%E4%B9%A0-%E6%95%B0%E6%8D%AE%E6%8C%96%E6%8E%98

如果真有10亿个新闻句子，nlp词的问题对一般的应该都够用了吧。 //@梁斌penny:后续我们还在build更大的模型，预计能分享10亿个新闻句子，大部分创业公司build模型应该是足够了。希望未来语料，模型，机器都可以免费提供，把创业梦想留给年轻的同志们。
@梁斌penny
为了证明pullword的有效性，我将分享1.4亿条新闻句子（未分词和pullword分好词后的，两份语料）大约40GB，希望大家喜欢，明天或者后天开放在pullword.com的首页下载专区中。

emnlp也被deep and semantics方面的词语占领了！ //@刘知远THU:标题中出现的词汇：model 39次，translation 33次，learning 26次，parsing 15次，network 15次，extraction 14次，joint 13次，representation 13次，topic 10次，graph 10次，relation 10次，embedding 9次，knowledge 9次，sentiment 8
@刘知远THU
EMNLP 2014 accepted paper list: O网页链接 祝贺各位！

人机交互-智能数据-人的协作和智慧-机器的计算和存储 Apple(iphone/ipad)-移动计算设备 Amazon(EC2/S3)-云计算和云存储 Facebook/Twitter-协作和数据(核心资产) Google(ML/NLP)-智能生活应用 在可穿戴智能计算时代，不知道现在的四大金刚会有怎样的发展，或者说创业者怎样找到适合自己的领域。

OpenRefine这类工具很重要啊，对知识库挖掘很有帮助。 //@西瓜大丸子汤:搭车推荐一下我以前的一篇博文《面向人机交互的内容理解》 http://baojie.org/blog/2013/11/22/hci-centric-nlp/ 这是我读了David Karger的一些文章后，结合自身工作写的一些读后感。
@鲍捷AI
http://semanticweb.memect.com/?tag=openrefine OpenRefine是一个数据清理的优秀工具。它根源于MIT David Karger实验室的研究。该实验室在交互式数据处理的前沿。David Huynh把这个研究带到MetaWeb，也即Freebase团队。被Google收购后，工具改称Google Refine。后来开源成为OpenRefine。这组资源包括了9个必读博客和教程

Mozilla/5.0 (X11; Linux x86_64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/33.0.1750.146 Safari/537.36

2014-7-28

国内的公司，还是比较看好百度的。希望在ai方面做更多的事情！ //@张栋_机器学习:百度在 AI 领域的大手笔投入会 "憋" 出一个甚至几个大招 [呵呵]
@韧在百度
百度致力于让 AI 无所不能 无处不在[酷]. "他认为，业内流行的'凡事皆云'，亦即一切处理和计算都在云端的技术已经过时，比如说微软近期公开的Project Adam，亚马逊Fire Phone，和脸书早些时候对外演示的狗的识别等, 这些都 'so yesterday'".... http://tech.qq.com/a/20140728/018726.htm

2014-7-29

Apollo 11号登月（1969年人类第一次登月）控制系统源代码，美国人真是超级给力，这么重要的系统都可以开源。 //@周枫zf:Nice，那个电脑我见过，只有一个手提箱大，那是1969年. //@刘江总编: 这些代码是从MIT博物馆（系统开发者是MIT仪器实验室）的纸版文献扫描、数字化出来的，今天还能在PC上运行，要
@蒋涛CSDN
Apollo 11号登月（1969年人类第一次登月）控制系统源代码欣赏 http://www.ibiblio.org/apollo/index.html @极客头条 @刘江总编

stackoverflow, instagram, whatsapp的经验，表示很理解很赞同。
@djvu9
stackoverflow, instagram, whatsapp的经验总结起来就几条：技术栈和编程语言是不重要的只要你有合适的人。十几个码农就可以做到很大规模，所以招人不如加工资。人少的时候就只能控制复杂度，代码和产品功能不太多，不瞎折腾流程，还尽量用现成东西，从而可以活得比较久。简单说就是：不作就不会死。

https://code.google.com/p/cuda-convnet/ cuda-convnet cuda-convnet2 Fast convolutional neural networks in C++/CUDA 确实是好东西！ //@梁斌penny:昨天在国立大学和几个深度学习内行学生交流，他们不care源码，只关心如何高效调参，代码拿到手，不会调参也没用，美军要把调参过程也一并开源啊。 /
@王威廉
谷歌Alex Krizhevsky写了一篇在GPU集群并行Convolutional Neural Network的文章 http://arxiv.org/abs/1404.5997 并且公开了源代码 https://code.google.com/p/cuda-convnet2/

https://github.com/jdeng/word2vec Word2Vec in C++ 11 http://nbviewer.ipython.org/github/dolaameng/tutorials/blob/master/word2vec-abc/poc/pyword2vec_anatomy.ipynb An Anatomy of Key Tricks in word2vec project with examples

现在deep方面的开源lib越来越多了。 //@西瓜大丸子汤:这个是特别热门的一个库，从算法和实现语言覆盖面上都是一网打尽，学习深度学习代码的必读之一
@好东西传送门
18个最热深度学习项目逐一介绍 7） Yusuke Sugomori（巣籠悠輔）的深度学习实现 O网页链接 。这个有近600星，提供了5种语言的实现：Python, C/C++, Java, Scala，囊括了各种主流深度学习算法：DBN, CDBN,RBM, CRBM,dA, SdA, LR等。所有18个项目 O网页链接

速途同归，大家都在搞多gpu并行计算来做deep learning。尤其佩服那些用gpu做移动端离线计算的。
@路遥_机器学习
Torondo的这套Deep Learning代码 https://github.com/TorontoDeepLearning/convnet 是我目前读过的最好的关于CNN的C++/CUDA代码。比Caffe和cuda-convnet读起来舒服多了。想听听高手们的意见。@老师木 @陈天奇怪 @antinucleon @G_Auss @异构并行计算-风辰

2014-7-30

自然界最神奇的工具，brains，minds，machines，neural networks！！！ //@西瓜大丸子汤:神经网络ANN被称为第一工具和最后一个工具。什么意思呢？对一个问题域没有认识的时候，就可以把各种特征统统扔进ANN里，它会好歹出一个结果。等有了领域知识，就可以优化用其他模型。但模型总有不可理解的误差，
@好东西传送门
@LDL_BIT 问：有哪些文章讲了多层感知器MLP的拟合能力问题？尤其是拟合多项式的能力？答：当使用非线性的激活函数，MLP是图灵完备的，可以模拟任何函数，当然包括多项式函数。这称为普适逼近原理（Universal approximation theorem）。深度学习则提高了逼近的效率。经典论文见 http://bigdata.memect.com/?tag=universal-approximation-theorem

不以软件为核心整合能力的，都会成为时代的弃儿。 //@西瓜大丸子汤:一年前我就做出这个预测了
@Linuxeden开源社区
【昔日大佬三星 渐显衰落之相】　三星第二季度净利润将创下两年来的最低值，没有想到，大佬三星是第一个露出衰落之相的。三星的走低，基本是重蹈HTC的覆辙。两者都是借Android的大势崛...全文链接→O网页链接

http://deeplearning.cs.cmu.edu/ Deep Learning Instructor: Bhiksha Raj Papers and presentations 论文整理的非常全面！！！

2014-7-31

graphlab越来越注重实际应用了，不知道底层的powergraph和graphchi现在怎么样了。 //@张栋_机器学习:GraphLab 降低了所有公司和程序员想开发机器学习应用的门槛
@陈天奇怪
重新发一遍-_- 大规模机器学习公司graplab大会keynote视频(要翻墙): O网页链接 。发布了新版本的GraphlabCreate。单机数据处理TB级别的数据，大数据可视化，包含了完整高效的机器学习工具，LDA, factorization machine, boosted tree。安装最新版本 O网页链接

http://yidianzixun.com/news_b2e0cbb41bfba142d80ff3752d36cf03?s=1 Scaled Inference欲成为所有人的Google Brain，获腾讯投资 腾讯最近在dl上开始大力投入了。 google内部人才流失停严重的啊，连Quoc V. Le都要创业去了。 大公司呆不得，即使是GOOGLE。

http://mp.weixin.qq.com/s?__biz=MTEwNTM0ODI0MQ==&mid=201104058&idx=1&sn=f6fe707c1edd85ba2abea6664871a651&scene=2&from=timeline&isappinstalled=0#rd 【腾讯深度学习系列】Mariana: 深度学习在腾讯的平台化和应用实践 第一篇
@tony的微博
O网页链接 Scaled Inference欲成为所有人的Google Brain，获腾讯投资 腾讯最近在dl上开始大力投入了。 google内部人才流失停严重的啊，连Quoc V. Le都要创业去了。 大公司呆不得，即使是GOOGLE。

http://www.vice.cn/read/david-whyte-creates-mind-boggling-geometric-gifs-using-processing 数学GEEk是这样玩迷幻的 那些神奇的代码构建的奇幻世界。 processing和openframeworks在移动时代会有更大的发挥空间。

http://www.vice.cn/read/make-it-wearable-the-concepts-sleep-hacking-with-iwinks?ref=tcp 可穿戴创想｜革新概念（5）：操控你的梦境 真正的智能可穿戴设备，可以让你的生活更美好！
@tony的微博
O网页链接 数学GEEk是这样玩迷幻的 那些神奇的代码构建的奇幻世界。 processing和openframeworks在移动时代会有更大的发挥空间。

http://www.vice.cn/read/leviathan-the-future-of-storytelling?ref=tcp 利维坦》计划——电影叙事的未来 intel在终端交互和云计算方面都有很多创新点。

http://www.vice.cn/read/[%E5%8F%AF%E7%A9%BF%E6%88%B4%E5%88%9B%E6%83%B3]-%E7%AC%AC%E4%B8%80%E9%9B%86%EF%BC%9A%E6%9C%AA%E6%9D%A5%E4%BA%BA%E7%B1%BB%E5%B0%86%E5%A6%82%E4%BD%95%E4%BA%A4%E6%B5%81%E6%B2%9F%E9%80%9Anew 未来人类将如何交流沟通
@tony的微博
O网页链接 《利维坦》计划——电影叙事的未来 intel在终端交互和云计算方面都有很多创新点。

http://www.vice.cn/read/Make-It-Wearable-Part-4-Becoming-Superhumannew 可穿戴创想 | 第四集：成为超级人类 Eidos让人控制并加强自己在现实中的感知能力。 Eidos视觉，和Eidos听觉。 //@tony的微博:O网页链接 未来人类将如何交流沟通
@tony的微博
O网页链接 《利维坦》计划——电影叙事的未来 intel在终端交互和云计算方面都有很多创新点。

Eidos视觉增强的是一般肉眼所无法看见的事物在空间里运行的轨迹，使用者带着Eidos所看到的景象有如一个巧妙PS的画面，但是它是动态和实时发生的。而Eidos听觉，则是重新定义了私人视听空间的概念，戴上它，你讲能够在一个吵杂的环境中选择你想听到的一个单独的声音，并将所有其他的杂音都隔绝在外。 //
@tony的微博
O网页链接 《利维坦》计划——电影叙事的未来 intel在终端交互和云计算方面都有很多创新点。

2014-8-1

Reducing the Sampling Complexity of Topic Models by Aaron Li, Amr Ahmed, Sujith Ravi, Alexander Smola 很赞
@李沐M
继wsdm后，alex和他的小伙伴们拿了今年KDD的best paper，他们做一个新的sampler，把LDA的优化加速了10倍。Reducing the Sampling Complexity of Topic Models by Aaron Li, Amr Ahmed, Sujith Ravi, Alexander Smola

这个不错
@骆逸
读了《The Architecture of Open Source Applications, Volume II》http://www.aosabook.org/en/ 中的几章，觉得这书太有价值了。在这本书里，世界上最牛的一批开源软件开发者详细讲解了他们是怎么做架构的。第二卷包括了Nginx、GDB、Git、Mailman、MediaWiki、MPI、SqlAlchemy、ZeroMQ等等。 绝对值得细读！

2014-8-2

单机性能非常重要，当然主要还是看应用，像nginx和redis这样的就非常好。 //@何_登成:PPT前半部分，探讨了在现有的硬件发展，尤其是CPU的发展趋势下（多核，低频），系统软件的Scale问题：Scale-up vs Scale-out。Scale-up，提升单线程处理能力；Scale-out，系统支持多线程（进程），提升并发处理能力
@何_登成
学习了@jametong 推荐的这篇PPT：Traditional Programming Models: Stone Knives and Bearskins in the Google Age http://qconlondon.com/dl/qcon-london-2009/slides/CameronPurdy_TraditionalProgrammingModelsStoneKnivesAndBearskinsInTheGoogleAge.pdf 真心不错，作者深谙可扩展系统的精髓！将其提出的可扩展系统5-Pattern图，组件保持不变，说明稍作替换，直接就变成了我们自主研发的分布式数据库系统DDB[吃惊]

simple is not simple //@梁堃-freearth:这个得转
@左耳朵耗子
做软件写代码，一定要明白——简单不是简陋，简单不是架飞线，简单不是怎么快怎么来，简单不是hack，简单是最复杂的事，达到简单是最花时间和精力的事，简单其实是最高的标准。


