---
layout: cn_post
title: 2014reading weibo信息轨迹7 deep learning
categories: [生活]
tags: [weibo]
---

2014-5-19

“今天，由于电子计算机的发展，大量工程计算都用上电子计算机了。对现代工程来说，数学似乎不那么重要了。我对这种趋向感到惋惜。在我看来，数学思维比数学运算更重要，只要有可能，就应该尽量鼓励学生学习和运用数学思维。”——冯·卡门

http://people.cs.umass.edu/~wallach/ http://dirichlet.net/ wallach 的topic models 文章一大把！ phd thesis："Structured Topic Models for Language." Ph.D. thesis, University of Cambridge, 2008.

http://blog.echen.me/2011/07/18/introduction-to-restricted-boltzmann-machines/ blog.echen.me Edwin Chen's Blog restricted-boltzmann-machines

http://www.cs.ubc.ca/~murphyk/Bayes/bnintro.html Graphical Models and Bayesian Networks By Kevin Murphy, 1998. Kevin Murphy 很久以前的文章了。

http://research.google.com/pubs/KevinMurphy.html Kevin P. Murphy google research 现在牛人越来越多了。 余凯老师将deep learning带到国内后，百度一直在跟随。 Andrew Ng 的加入，让一些信心不够的人深入下去。 就会知道，这一次确实不一样。

2014-5-20

"360有一段时间也很狂热地做各种App，但是后来我突然发现，这不是我核心竞争力，我也做不好，因为你做十件正确的事，不如你把两件正确的事一件一件做得最大。" 很认同！

作为Max/MSP和PureData的发明人，Miller Puckette在computer music领域的影响极为深远。这两款特为音乐家开发的编程工具堪称dataflow & visual & live programming的典范。此次有幸能当面向他请教让我更清楚地认识了其背后的设计理念，颇有启发! --赞！！！

Miller Puckette 他的topic是谈交互式音乐软件的新方向，按我的理解核心部分是这个问题：computer作为演奏工具如何更好地表达音乐的实时动态演进；作为作曲工具如何更自然地表达完整的音乐意图？这两方面很多时候是互相矛盾的，如何更好地协调统一？我相信这也是所有互动创---赞！！！

经过不懈的努力，Geoff Hinton及其弟子终于用Deep Boltzmann Machine捣鼓出了类似LDA的隐变量文本模型，号称其抽取的特征在文本检索与文本分类上的结果比LDA好。UAI2013论文 http://www.cs.toronto.edu/~nitish/ toronto Nitish Srivastava 期待各种document级别的应用出现。

LDA和RBM 都是捕捉了 bag of words 表达中各 word 之间的统计关系，都是 latent variable model， 但前者是所谓mixture model，各 topic 之间是 sum 关系，后者是所谓 product of experts model，各 topic 之间是 product 关系 hinton 说后者可以产生更 sharp 的分布二者能硬写成一样的结构 -老师木

lda结构是word-hidden topic。类lda结构假设在topic下产生每个word是条件独立而且参数相同。这种假设导致参数更匹配长文而非短文。这篇文章提出word-hidden topic-hidden word，其实是(word,hidden word)-hidden topic。增加的hidden word平衡了参数对短文的适配，在分类文章数量的度量上更好很自然。

http://www-cs.stanford.edu/~quocle/ stanford Quoc V. Le Tomas Milkolov 在ICML 2014 上发表的 Distributed Representations of Sentences and Documents，终于可以下载了。

http://arxiv.org/abs/1405.4402 1405.4402 Towards Topic Modeling for Big Data Yi Wang Zhihui Jin

2014-5-21

http://journals.cambridge.org/action/displayAbstract?fromPage=online&aid=9155271 journals.cambridge.org A tutorial survey of architectures, algorithms, and applications for deep learning by Li Deng

http://www.toptal.com/machine-learning/an-introduction-to-deep-learning-from-perceptrons-to-deep-networks toptal.com An Introduction to Deep Learning: From Perceptrons to Deep Networks

http://www.kdnuggets.com/2014/02/exclusive-yann-lecun-deep-learning-facebook-ai-lab.html kdnuggets.com Interview with Yann LeCun

http://colah.github.io/posts/2014-03-NN-Manifolds-Topology/ colah.github.io Neural Networks, Manifolds, and Topology

神经网络能卷土重来，个人认为，最重要的贡献来自Schmidhuber组。没有任何保障，兴师动众，上GPU，把风险都承担了，多个竞赛拿第一，让大家看到实在的成果，才有这么多人愿意follow，承担的风险也小得多。这浪潮光靠Hinton系发paper是推不动的。但是听说Schmidhuber做人有问题，一直没得到业界 哈哈

http://deeplearning.stanford.edu/wiki/index.php/%E7%A5%9E%E7%BB%8F%E7%BD%91%E7%BB%9C deeplearning.stanford.edu 翻译

数学物理学家John Baez在牛津大学关于 category theory 的讲座，从 categorical theoretical perspective 来解释 entropy & bayesian reasoning. Category theory 在数学物理界一直被认为太pure,找不到 practical application, 但现在牛津大学把它用到了信息论中。category theory 貌似要hot起来 哈哈

http://www-etud.iro.umontreal.ca/~goodfeli/ www-etud.iro.umontreal.ca Ian Goodfellow 2013 Google PhD Fellowship

最近越来越多的体会到，cv的各个问题，从粗到细，classification，detection，pose estimation（alignment），segment，parsing，每个模块都可以用deep learning解决，而且，越多的将上述的不同问题一起考虑，越可能得到更好的结果（区别于孤立的将每个问题分开处理）。 赞！！！

deep learning在工程上面的优势，在于更少的hand-crafted，更多的automatic，在于feature learning，一药包治百病；而能取得好效果的关键在于，大规模的数据以及运算资源的支持，模型、数据、运算资源缺一不可。赞！！！

其中，detection，由于速度，在类别少（比如两类），特别是人脸、人体等pattern相对简单的情况下，boosting这种快速表示能力中等的模型会占优势，但是，当类别数目多情况下，deep learning的distributed结构，由于parameter share，反而在速度上可能会有优势。赞！！！

DL在机器翻译上也显示威力了。BBN用DNN训练LM和TM的joint model在他们最强的系统上提高了2-3个bleu.甩开了所有BOLT groups一大截。在hiero baseline上提高6-7个bleu.去年9月份就知道这个消息了，但是直到今天他们自己公布出来才可以说。他们的文章投给ACL了。赞！！！

http://techblog.netflix.com/2014/02/distributed-neural-networks-with-gpus.html netflix Distributed Neural Networks with GPUs in the AWS Cloud 好多用aws做deep learning了应用出现。

Deep Convolutional Neural Network一年前还只能用于recognition/classification, 现在都能object detection了, 一篇google 2013 NIPS http://machinelearning.wustl.edu/mlpapers/paper_files/NIPS2013_5207.pdf 一篇Andrew Ng组的Archiv paper http://arxiv.org/pdf/1312.6885.pdf 另一篇Jitendra Malik组paper http://arxiv.org/pdf/1311.2524.pdf 赞！！！

Tensor最近在NLP开始流行，从spectral learning (Cohen)到word tensor (Kartsaklis), multi-relational LSA (Chang)和recursive neural tensor network (Socher)。赞！！！ 期待各种其他模型和方法！

今天present了一篇scene labeling的paper, 当然用到CRF啦，因为graphical model是structured prediction的典范，embedding of semantic information直观，但不得不说在有higher order clique的GM中，inference很耗时，而且没有bound guarantee, 加上cross validation, GPU coding成为研究它的必需 赞！

2014年美国科学院院士名单公布，UCLA的Judea Pearl和Stanford的Emmanuel Candes入选。Judea Pearl大神2011年获得图灵奖，代表工作包括graphical model和causal inference；Emmanuel Candes的代表工作是compressive sensing。http://www.nasonline.org/news-and-multimedia/news/april-29-2014-NAS-Election.html 赞！！！

王威廉 ICML2013其实有两个Classic Paper Awards：分别授予了十年前CMU Zhu, Ghahramani, Lafferty关于图label propagation半监督学习经典工作 （ICML2003论文 http://www.aladdin.cs.cmu.edu/papers/pdfs/y2003/zgl.pdf），以及当时CMU另一名学生Zinkevich关于online learning的经典之作(ICML2003论文 http://martin.zinkevich.org/publications/ICML03.pdf 。赞！！！

CMU毕业生Jerry Zhu当年在LTI读博士期间与其导师John Lafferty等人所撰写的半监督学习论文，经过10年时间的考验，终于被ICML 2013授予了经典论文奖（ICML 2013 Classic Paper Prize）。Jerry Zhu是半监督学习的专家，曾经写过一本半监督学习的专著。Lafferty发明了CRF。经典论文：http://machinelearning.wustl.edu/mlpapers/paper_files/icml2003_ZhuGL03.pdf

Rise of Machines, written by Larry Wasserman. 统计学家高度评价了machine learning “If You Can't Beat Them, Join Them” http://www.stat.cmu.edu/~larry/Wasserman.pdf 赞！！！www.stat.cmu.edu larry Wasserman


在机器学习国际大会（ICML）上John Lafferty, Andrew McCallum, Fernando Pereira的关于条件随机场的论文获得了时间考验奖（Test-of-Time Award ）。该奖项授予现在评价的10年前ICML最佳论文。条件随机场已被广泛应用到信息抽取、自然语言处理等领域。赞！！！



