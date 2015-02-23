---
layout: cn_post
title: 2014reading weibo信息轨迹8 machine learning
categories: [生活]
tags: [weibo]
---

2014-5-22

数学和程序语言完全是相通的：1.都是人为设计的模型，比如线性代数就是一门DSL；2.都有自己的语法和语义，比如线性代数的矩阵运算规则语法和线性变换语义；3.都有抽象层次，数学定理其实就是程序的可复用库；4.都可以用其他模型解释，比如用解析几何模型解释线性代数其实就是程序的编译和解释。赞！

关于编程，我认为最重要的是模型思维，要区分模型和模型的表达方式。以模型的观点，数学和程序没有什么不同，如线性代数就是一门DSL，它有自己的语法（矩阵和运算规则）和语义（线性变换），同时线性代数又可以用解析几何等模型解释，这就是编译器/解释器。模型本身有无穷多，模型的表达方式可以统一赞

维基百科，大规模生语料，平行及复述语料，可以玩出很多有意思的东东。而graphical model，基于图的半监督算法，整数规划和dual decomposition，俨然已经成为log/global linear model和标准线性代数工具之外的NLP标配。深度学习在文本处理上貌似目前能突破历史成绩的任务还不多。赞！！！

发现shallow NLP基本上就是美国结构主义语言学的路子啊。先收集和标注语料，搞定前记录和同一性认定；然后主要采用各种distribution演化出的特征，建立log linear, global linear, max margin等模型去分类，或者基本线性代数工具等方法去聚类。赞！！！

Scikit-learn想必用过Python做数据挖掘的同学都用过吧，单机做完实验之后把算法搬到大数据平台上？用Mahout或者MPI重写？或者干脆采样别跑全量了。如果有人把Scikit-learn移植到目前最流行的Spark平台上大家怎么看？ https://github.com/scikit-learn/scikit-learn/wiki/Upcoming-events 赞！！！

很有意思的机器学习四大基本任务算法流程图（scikit-learn）：主要是讲的是如何根据数据的特点，应该怎么选择机器学习的具体任务（分类、聚类、回归、降维），同时间接地指出了这四个任务的区别与联系。对于入门者来说的话，可以考虑打印出来，贴在墙上。大图在这里： http://1.bp.blogspot.com/-ME24ePzpzIM/UQLWTwurfXI/AAAAAAAAANw/W3EETIroA80/s1600/drop_shadows_background.png 赞！

Computer Science最伟大的地方我觉得就是一个是easy to try，另一个就是build on free，等等。同时体现了这两点，并且在focus在machine learning领域的就是：scikit-learn。向大家强烈推荐这awesome的python的机器学习工具包，特别是对于想做各种实验的人。赞！！！

随机梯度下降跟凌波微步神似 若要用武功比喻，那么ML是融汇众长的北冥神功，倘自身修为不够，就降级成吸星大法，短时很牛，时间长了会反噬。入门先站三年桩是错不了的。@李沐mu: 1是内力，2是轻功。ML只是招式 //@马毅微言: 要想学好ML，我建议先好好学学1.高等数理统计；2.优化方法。赞！！！

前几天听过N G的讲座后，感觉只有搞神经的是在做研究，什么图像啦，语音啦，ML啦，都是应用，最火的DEEP也是应用。 赞！！！ 认知科学，神经科学等基础是本源。

Do Deep Nets Really Need to be Deep? 微软研究员Rich Caurana近日在arxiv发文，认为深度学习的深层次模型其实可以用浅层次模型来模拟表示。http://arxiv.org/pdf/1312.6184v1.pdf 谷歌研究主任Fernando Pereira认为这一点也不奇怪，早在89年就有文章说明1层MLP的表达能力与多层神经网络相同。 http://pages.ucsd.edu/~hwhite/pub_files/hwcv-028.pdf 赞

@Hyperddr: 虽然表达能力是一样的，但面对同样的问题，浅层网络需要的神经元的数量是大得多的，而且泛化能力肯定不及deep。赞！！！

感知机算法是理解deep learning的开端。强烈推荐1958年的一篇论文《The perceptron: A probabilistic model for information storage and organization in the brain. 》 文中提出三个问题：1）生物系统如何感知物理世界的信号 2）信息存储的形式 3）存储的信息是怎么产生识别和判断能力的 赞！！！

从生理数据上，人们对early vision神经元行为了解多一些，对于high level行为了解还很有限，连行为都不了解更谈不上理论理解了。但有人相信efficient coding类似原理应该在high level partially holds。我觉得deep learning就可以视为该原理向高层的推广，不过无监督学习的作用现还存疑。赞！！！

梁：最近看的几个东西：Energy-Based Learning；Representation learning; 概率图模型。其实这些东西里面既有区别，又有联系，但以我现在读论文的水平和能力还打不到打通的水平，还在做试验，通过coding论文中例子加深理解，估计按照现在这个读论文的速度，预计还要读2-3年才能达到美军初级水平 赞！

强烈推荐『Mining Text Data』这本书，从文本聚类、分类、主题模型、概率图模型到信息抽取情感分析基本把文本挖掘每个部分都涵盖了。赞！！！

我觉得LDA是近十年来CS领域第一大坑... overparameterization与non identifiability等缺点就不多说了。 当然LDA还是很有意义的：对词特征long range dependency建模挺有意思，对普及概率图模型，variational inference和Gibbs sampling的经典推断方法影响很大。赞！！！

近年机器学习的博士论文：Xiaojin Zhu的“Semi-Supervised Learning with Graphs”和Ben Taskar的“LEARNING STRUCTURED PREDICTION MODELS: A LARGE MARGIN APPROACH”，一个在威斯康辛做AP，一个在Upenn做AP；一个从概率图的角度研究机器学习，一个从maximal margin的角度研究图模型的学习。赞！！！

消除歧义，是人工智能的重要问题，自然语言处理，语音图像视频理解概莫能外。消歧得诉诸上下文，具有多义性的句子或词汇在特定上下文中出现时，通常多种含义中只有一种理解是和谐的。落实到算法上，最优美的就是概率图模型了，例子包括早些年隐马尔科夫模型到现在流行的条件随机场。赞！！！

3）当然可以说，硅晶何必和碳晶一样，那么Deep Learning的源头还是在Hubel & Wiesel的视觉神经机制的基础之上的。而且1960年代左右的成果，大约1990年代才进入ML的范围，而cogitive和neuro还在一直发展的 赞！！！

2014-5-24

http://www.reddit.com/r/MachineLearning/comments/25lnbt/ama_yann_lecun/ reddit Yann LeCun machine learning

"Web Development" 这门课除了原理更注重实践，python框架用的是webapp2, 作业是写一个blog，直接在google app engine上搭建和提交；授课老师是Reddit创始人，Reddit目前的流量貌似世界前100名，但是只有3个工程师，课程有一小节专门采访相关的工程师聊Reddit当前的架构，干货非常多。赞！！！

so what does it mean ???
震惊！Aaron Swartz自杀身亡，年仅26。他是Reddit的联合创始人，web.py的设计者，14岁参与创造了RSS 1.0规范，又与John Gruber共同设计了Markdown。2011年曾因下载480万篇JSTOR学术论文而被捕。http://tech.mit.edu/V132/N61/swartz.html
so what does it mean ???

http://www.reddit.com/r/MachineLearning/comments/1ysry1/ama_yoshua_bengio/ reddit Yoshua Bengio machine learning

http://nbviewer.ipython.org/github/CamDavidsonPilon/Probabilistic-Programming-and-Bayesian-Methods-for-Hackers/blob/master/Prologue/Prologue.ipynb Probabilistic Programming and Bayesian Methods for Hackers Using Python and PyMC

孩子初学母语的时候，往往是“无监督”和“半监督”的，到了学外语的时候就变成“有监督”的了，而我们一般都是母语说的比外语好。这是不是能从另外一个角度解释为什么deep learning效果比较好而且有前途啊。赞！！！

2014-5-25

http://cxwangyi.github.io/story/html/03_rephil_and_mapreduce.md.html cxwangyi.github.io Rephil和MapReduce hierarchical Dirichlet process（HDP）

http://www.dapenti.com/blog/more.asp?name=xilei&id=90082 dapenti.com [人物]90后创业者：我和你们不一样 --我们都老了！

http://www.iqingang.com/post/19 iqingang.com 秦刚：垂直自明星，下一个互联网金矿（完整版） any way, it's the time about personality intelligence computing.

O网页链接 marklol.com 成立仅8个月的个人网站，月收入几十万美金 几个月前看到的文章，现在仍然感到很震惊！

viralnova.com 必须要知道那些是用户真正所需。硬性需求！

marklol.com 另类电商Amazon评论中掘金，年入上亿美金 any way，还是国外的东西简单，事情好做。

O网页链接 marklol.com 互联网创业的“南派”和“北派” 南派务实，北派务虚 南派屌丝性创业，北派高富帅创业 南派重服务，北派重炒作 不知道上海这个中间派，算什么呢？

2014-5-26 

http://blog.smola.org/ smola.org Adventures in Data Land Distributing Data in a Parameterserver

MI Jordan发表了78篇NIPS和25篇ICML，Geoff Hinton发表52篇NIPS和10篇ICML，Alex Smola发表39篇NIPS和18篇ICML, Tomaso Poggio发表38篇NIPS和1篇ICML 赞！！！

2014-5-27

http://www.scientificamerican.com/article/twitter-to-release-all-tweets-to-scientists-a-trove-of-billions-of-tweets-will-be-a-research-boon-and-an-ethical-dilemma/ Twitter to Release All Tweets to Scientists A trove of billions of tweets will be a research boon and an ethical dilemma

http://vincent.vanhoucke.com/publications vincent.vanhoucke.com Multiframe Deep Neural Networks for Acoustic Modeling ... many papers about speech research

2014-5-28

理解傅里叶变换，我推荐一个最简单的例子：看几个数字010101...01，001001001...001，... 这些数字的规律表现为“1的出现频率是x”。如果通信内容都具备这个规律，通信双方就可以约定：“以后不需要发送完整数字，只需要发送这个频率值”，这样就达到了压缩的效果，整个过程就是时域和频域的映射 赞！

西瓜大丸子汤 如果真如Cheyer说的那样，是Jobs坚持做语音界面，那就和当年的爱疯天线门一样，是Jobs以他天才的现实扭曲力场，试图扭曲技术规律的行为。遗憾的是，电磁波定律无法被扭曲，人工智能的的规律也无法被扭曲。赞！！！

http://yima.csl.illinois.edu/Publication.html yima.csl.illinois.edu Publications of Yi Ma http://sist.shanghaitech.edu.cn/index.asp sist.shanghaitech.edu.cn ShanghaiTech University



