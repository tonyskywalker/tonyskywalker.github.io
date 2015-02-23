---
layout: cn_post
title: 2014reading weibo信息轨迹9 deep mind
categories: [生活]
tags: [weibo]
---

2014-5-29

http://recode.net/2014/01/27/more-on-deepmind-ai-startup-to-work-directly-with-googles-search-team/ recode.net More on DeepMind: AI Startup to Work Directly With Google’s Search Team

https://gigaom.com/2014/01/29/google-isnt-the-only-company-working-on-artificial-intelligence-its-just-the-richest/ gigaom.com Google isn’t the only company working on artificial intelligence. It’s just the richest

http://spectrum.ieee.org/automaton/robotics/home-robots/interview-scott-hassan-on-willow-garage-and-the-future-of-suitable-tech Interview: Scott Hassan on Willow Garage and the Future of Suitable Technologies

http://www.theguardian.com/technology/shortcuts/2014/jan/28/demis-hassabis-15-facts-deepmind-technologies-founder-google theguardian.com Demis Hassabis: 15 facts about the DeepMind Technologies founder

http://www.theguardian.com/technology/2014/feb/22/robots-google-ray-kurzweil-terminator-singularity-artificial-intelligence theguardian.com Are the robots about to rise? Google's new director of engineering thinks so…

2014-5-30

http://cbcl.mit.edu/people/poggio/poggio-new.htm Tomaso Poggio learning the core of the problem of intelligence, both biological and artificial the gateway to understanding how the human brain works and for making intelligent machines CBCL studies the problem of learning within a multidisciplinary approach

brain mathematical computer statistical learning. Three basic directions of research : mathematics of statistical learning theory, engineering applications (in computer vision, computer graphics, bioinformatics and intelligent search engines) and neuroscience of visual learning

这几位都在该领域研究几十年了，毕生的成果积累啊！ //@欧长坤:为何这么高产 //@星空下的巫师: Tomaso这么不受ICML待见？
@tony的微博
MI Jordan发表了78篇NIPS和25篇ICML，Geoff Hinton发表52篇NIPS和10篇ICML，Alex Smola发表39篇NIPS和18篇ICML, Tomaso Poggio发表38篇NIPS和1篇ICML 赞！！！

2014-5-31

http://www-lium.univ-lemans.fr/~schwenk/ Holger Schwenk many papers on neural networks language model translation speech

2014-6-4

http://www.utc.fr/~bordesan/dokuwiki/doku.php?id=en:publi Antoine Bordes many Entities Mining and Knowledge Bases papers

自从知道 www.aol.com 的搜索用的也是 google搜索之后, 我就用aol上瘾了. 因为 aol的搜索有个优点: 搜索结果和google一样,但是#搜索结果中的链接都是直接给出的目标链接#, 而google的都要通过google转一下,又慢有麻烦. 所以, 大家都来用aol吧. 赞！！！

http://leon.bottou.org/papers Léon Bottou From machine learning to machine reasoning: an essay

http://www.thespermwhale.com/jaseweston/ thespermwhale Jason Weston many papers Research Scientist at Facebook, NY, USA.

http://www.cs.toronto.edu/~nitish/ Nitish Srivastava Improving Neural Nets with Dropout Masters Thesis, University of Toronto, Jan 2013

http://www.cs.toronto.edu/~rsalakhu/publications.html Ruslan Salakhutdinov many papers about deep learning and Deep Boltzmann Machines

honglak lee的看法也很给力：他说人类从婴儿到长大成人，无数的图像（视觉）输入其实大多数都没有给显式的label，所以可以说是无监督学习长大的。赞！！！

http://web.eecs.umich.edu/~honglak/ Honglak Lee many papers about Deep Learning and unsupervised feature learning

https://www.cs.toronto.edu/~ilya/pubs/ Ilya Sutskever co-founder of DNNresearch Training Recurrent Neural Networks PhD Thesis, 2012

http://cs.stanford.edu/~quocle/publications.html Quoc V. Le Distributed Representations of Sentences and Documents ICML, 2014

http://suvrit.de/chron.html suvrit sra focus on optimization in machine learning

http://www1.icsi.berkeley.edu/~vinyals/publications.html Oriol Vinyals deep learning speech and language

http://www.danielpovey.com/publications.html Dan Povey's publications and kaldi speech toolkits http://kaldi.sourceforge.net/

突然觉得rectifier和dropout、maxout有点如初一折啊，rectifier在某些地方hard的设置激活值为0，后两者是用一定的方法设置为0，造成激活值的稀疏，稀疏带来的好处就不说了。。rectifier还好的一点就是，还可以在某些地方不让梯度消失，因为他的导数是1 ---赞！！！

三者的主要贡献在于减少无关神经元被修改。每个神经元都是一个模式识别器，传统bp不管来的是什么模式，所有神经元都会被多少被修改。relu禁止较无关的一半神经元被修改，maxout禁止大多数，drop随机禁一半。---赞！！！

dropout的insight在哪里呢?其实医学界早就在癌症治疗上用了很久很久了,那就是化疗: 首先假设大多数细胞都是好的,癌细胞只是极少数.所以我随机杀掉一部分,误杀了好细胞没关系,要是正好把那极少数癌细胞杀了,那就皆大欢喜.个人并不喜欢dropout,还是maxout更有insight,人家那是靶向治疗,虽然还得配化疗？

http://fastml.com/deep-learning-these-days/ fastml.com Deep learning these days

2014-6-5

回复@一只猴子啦:我觉得视觉识别还涉及高层的概念和知识，视觉和语言到了高层表示是很难分开的。 人在幼儿时段更多的收到大人的指导，即使长大了可以自我学习，也是建立在整个社会知识体系的基础之上的。个人不断试错，社会正负反馈，个人快速改进，如此循环。人的每一天都在受到他人的直接或间接影响
@tony的微博
honglak lee的看法也很给力：他说人类从婴儿到长大成人，无数的图像（视觉）输入其实大多数都没有给显式的label，所以可以说是无监督学习长大的。赞！！！

回复@一只猴子啦:目前的机器学习方法，我非常看好4个概念，deep learning的深层结构，reinforcement learning的试错反馈机制，online learning的长时间持续训练，unsupervised learning的特征自动提取，希望以后会有更好的统一模型集各家之长。 //@一只猴子啦:其实，几乎所有做NN的人都是这么想的呢。

http://www.jair.org/vol/vol49.html jair.org journal of artificial intelligence research Volume 50 - Volume 1

http://www.cs.toronto.edu/~vmnih/ Volodymyr Mnih research scientist at Google DeepMind Playing Atari With Deep Reinforcement Learning Machine Learning for Aerial Image Labeling PhD Thesis, University of Toronto, 2013

http://www.cs.berkeley.edu/~pabbeel/ Pieter Abbeel Apprenticeship Learning and Reinforcement Learning with Application to Robotic Control Ph.D. Dissertation, Stanford University, Computer Science, August 2008

http://www.cs.cmu.edu/~zkolter/publications.html J. Zico Kolter many papers about machine learning and optimization Learning and Control with Inaccurate Models Ph.D. Thesis, Stanford University, 2010

http://www.matthewzeiler.com/pubs/ matthew zeiler many papers about Deep Convolutional Neural Networks Hierarchical Convolutional Deep Learning in Computer Vision Unpublished PhD Thesis (Nov 8, 2013)

http://schaul.site44.com/publications.html Tom Schaul machine learning researcher at Google DeepMind in London reinforcement learning and optimization with minimal hyperparameter tuning and (deep/recurrent) neural networks

http://koray.kavukcuoglu.org/publications.html Koray Kavukcuoglu research scientist at Google DeepMind Learning Feature Hierarchies for Object Recognition PhD Thesis, Jan. 2011 Learning word embeddings efficiently with noise-contrastive estimation Natural Language Processing (Almost) from Scratch

ICML 2014： zoubin Ghahramani 一次灌了8篇啊！Tong Zhang 4篇，Jun Zhu4篇，Bernhard Schoelkopf灌了4篇， Jieping Ye 6篇，Le Song4篇，Max Welling 4篇，Pradeep Ravikumar 5篇，Ryan Adams 5篇，Shie Mannor 6篇，deep learning的大潮下，大家都疯了！

http://mlg.eng.cam.ac.uk/zoubin/ Zoubin Ghahramani Probabilistic Models for Unsupervised Learning 1999

2014-6-6

blog http://brenocon.com/blog/ brenocon.com AI and Social Science – Brendan O'Connor cognition, language, social systems; statistics, visualization, computation

blog http://andrewgelman.com/ andrewgelman.com Statistical Modeling, Causal Inference, and Social Science

2014-6-8

阳志平1949 看到非言语 等老师为google学术被封着急：1）启用chrome浏览器的quic协议：在地址栏输入chrome://flags/ ，打开Quic相关的两个选项，再重启即可，只支持Google系列；2）使用史上最稳定的免费利器，但需要信用卡账号：privatetunnel.com；3）购买付费的，云梯还可以，Ruby社区朋友开发。赞

book https://probmods.org/ probmods.org Probabilistic Models of Cognition by Noah D. Goodman and Joshua B. Tenenbaum

book http://health.adelaide.edu.au/psychology/ccs/teaching/ccs/ health.adelaide.edu.au Computational Cognitive Science

book http://www.frontiersin.org/blog/Computational_Neuroscience_and_Cognitive_Modelling/621 frontiersin.org Computational Neuroscience and Cognitive Modelling: A Student's Introduction to Methods and Procedures

2014-6-14

http://makerhacker.github.io/blog-mining/nathan_marz_storm/nathan_marz_storm_home.html nathan marz (storm author) knowledge graph for his blogs

http://makerhacker.github.io/blog-mining/high_scalability/high_scalability_home.html high scalability knowledge graph for his blogs similar blogs computed by tfidf model and lsi model and lda model

http://makerhacker.github.io/blog-mining/hunch_net/hunch_net_home.html hunch_net knowledge graph for his blogs similar blogs computed by tfidf model and lsi model and lda model

早在两年多以前，谷歌董事长施密特就认为，如果有云计算作为后台服务的支持，把大量的手机攒起来，就有可能演变成超级计算机。在巴塞罗那电信展上，HTC推出“Power To Give”计划，正是对施密特想法的实践。
@老师木
想做一个系统，像bitorrent机制一样，利用亿万空闲个人pc的计算资源，来完成有意义的计算任务，包括大规模机器学习，用户可以提交job，参与计算的用户可以分享利益。bitcoin那样大量资源浪费在无意义计算上太可惜了。

我以为mpi差不多实现了这个目标//@陈天奇怪:说个自己粗浅的想法，感觉不一定要让代码往系统上面靠。 代码写的好，或许也可以让系统往算法上面靠。如果可以让机器学习算法依赖于少量的同步接口，不同框架实现这个接口，让一个代码在各种平台上面跑，似乎也挺好玩 赞！！！

http://alex.smola.org/index.html Alexander J. Smola Researcher, Google Professor, Carnegie Mellon University INTRODUCTION TO MACHINE LEARNING






