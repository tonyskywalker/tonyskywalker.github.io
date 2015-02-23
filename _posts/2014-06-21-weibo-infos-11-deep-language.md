---
layout: cn_post
title: 2014reading weibo信息轨迹11 deep language
categories: [生活]
tags: [weibo]
---

2014-6-21

http://www.mademan.com/chickipedia/ 语义网技术年度最佳应用，后台是Semantic Mediawiki。不解释(也就是说在办公室就不要点开了) 可以理解为美女且仅有美女的知识图谱。轻量级无固定模式的结构化数据录入，演进。数据在页面间流动。可以直接在页面里写查询，前后端一体 赞！！！

Gartner的Hype Cycle（发展规律周期）包含Gartner对众多行业发展周期的预测与判断。语音语义相关的有：语音识别（应该指的是通用识别）在2-5年内会进入产业应用爆发，虚拟助理的热潮已经在减退，但是2-5年同样进入应用爆发。相对来说自然语言的自动问答、语音翻译等还需要等5-10年。赞！！！

热潮退去的时候，就是该行动的时候！
@tony的微博
Gartner的Hype Cycle（发展规律周期）包含Gartner对众多行业发展周期的预测与判断。语音语义相关的有：语音识别（应该指的是通用识别）在2-5年内会进入产业应用爆发，虚拟助理的热潮已经在减退，但是2-5年同样进入应用爆发。相对来说自然语言的自动问答、语音翻译等还需要等5-10年。赞！！！

2014-6-22

http://blog.jobbole.com/70548/ Dropbox经验谈：iOS和Android的C++跨平台开发 分享了他们在移动 App 开发方面的经验。App 如何才能做到同时支持 iOS 和 Android 两个平台而又不需要在每个平台上对相同的功能重复编码。 Dropbox 的开发人员 Stephen Poletto 和 Sean Beausoleil 在给 Facebook 的开发人员做讲座

http://nautil.us/blog/the-math-trick-behind-mp3s-jpegs-and-homer-simpsons-face nautil.us The Math Trick Behind MP3s, JPEGs, and Homer Simpson’s Face 傅里叶变换：MP3、JPEG和Siri背后的数学

https://medium.com/@_marcos_otero/the-real-10-algorithms-that-dominate-our-world-e95fa9f16c04 medium.com The real 10 algorithms that dominate our world

http://io9.com/the-10-algorithms-that-dominate-our-world-1580110464 io9.com The 10 Algorithms That Dominate Our World

https://medium.com/the-physics-arxiv-blog/the-face-recognition-algorithm-that-finally-outperforms-humans-2c567adbf7fc medium.com The Face Recognition Algorithm That Finally Outperforms Humans Computer scientists have developed the first algorithm that recognises people’s faces better than you do

https://medium.com/@arxivblog medium.com The Physics arXiv Blog An alternative view of the best new ideas in science. About: tinyurl.com/p6ypk56

哈哈，research need to find the deepest principals！
@支持向量姬
为了读懂word2vec的论文，里面的hierachical softmax说依赖于morin and bengio(2005)，于是去读morin这篇文章，说它在优化bengio(2003)的模型，于是去下bengio这篇文章，读了半天，然后它说根据hinton(1986)的原理，然后我吐血了（

Steve Renals算了一下icassp录取文章题目中包含deep learning的数量，发现有44篇，而naacl则有0篇。有一种说法是，语言（词、句子、篇章等）属于人类认知过程中产生的高层认知抽象实体，而语音和图像属于较为底层的原始输入信号，所以后两者更适合做deep learning来学习特征。---1年前
@tony的微博
ACL 2014 长文的全文共出现 word2vec 39次，LDA 256次，SVM 216次，deep learning 43次，neural network 425次，sentiment 1016次，wikipedia 301次，Chinese 728次，English 852次。word2vec 很给力的工具！！！

NAACL今天的tutorial包括了斯坦福Richard Socher和Christopher Manning关于深度学习在NLP中应用的教学讲座。看了一下slides，比去年ACL的版本增加了一些新内容，可以算是关于深度学习在语言技术的应用中相当全面的tutorial了。"Deep Learning for NLP (without Magic)" ---2013年进展
@tony的微博
ACL 2014 长文的全文共出现 word2vec 39次，LDA 256次，SVM 216次，deep learning 43次，neural network 425次，sentiment 1016次，wikipedia 301次，Chinese 728次，English 852次。word2vec 很给力的工具！！！

词聚类：词义相似度可以分为两个角度来看：横向组合(syntagmatical) 和纵向聚合(paradigmatical)相似性。从语义分析来看，后者更为有用。经典的Brown聚类更倾向计算横向组合相似性。word2vec是计算纵向聚合相似性。 //@tony的微博:哈哈，research need to find the deepest principals！
@支持向量姬
为了读懂word2vec的论文，里面的hierachical softmax说依赖于morin and bengio(2005)，于是去读morin这篇文章，说它在优化bengio(2003)的模型，于是去下bengio这篇文章，读了半天，然后它说根据hinton(1986)的原理，然后我吐血了（

dan klein的博士论文: word的context延展至全文，且不考虑词的位置（bow)就变成了topic model之类，more semantic，当context很小且考虑位置就是distributional clustering，more syntax //@tony的微博:哈哈，research need to find the deepest principals！
@支持向量姬
为了读懂word2vec的论文，里面的hierachical softmax说依赖于morin and bengio(2005)，于是去读morin这篇文章，说它在优化bengio(2003)的模型，于是去下bengio这篇文章，读了半天，然后它说根据hinton(1986)的原理，然后我吐血了（

大体上是这样，几个决定性的component,1）windows的大小（5-words，句子, 文章, decay with distance），2)是否考虑语序， 3)词之间interaction的方式（linear/nonlinear, coherence/prediction, error function） //@tony的微博:哈哈，research need to find the deepest principals！
@支持向量姬
为了读懂word2vec的论文，里面的hierachical softmax说依赖于morin and bengio(2005)，于是去读morin这篇文章，说它在优化bengio(2003)的模型，于是去下bengio这篇文章，读了半天，然后它说根据hinton(1986)的原理，然后我吐血了（

dan klein 牛人何其多！！！ nlp，ml，cv，ai。。。
@刘洋THU
无意中发现Percy Liang已经毕业了。此大牛出身名门，本科和硕士在MIT（导师：Michael Collins），博士在Berkeley（导师：Michael Jordan和Dan Klein）。第一作者论文有6篇ICML、2篇NIPS、5篇ACL、3篇EMNLP、3篇NAACL，现在是Stanford的Assistant Professor：O网页链接。

很赞啊，nlp 牛人云集
@西瓜大丸子汤
O网页链接 直播：自然语言理解和计算语言学重要研究学者大全。比较重要的研究团队，只要现在还在活跃的（主页没挂掉的），应该都包括进去了。几百个组，现在每分钟都在往里加，请勤按F5刷新。可搜索，有图有真相。欢迎补充 @算文解字 @白硕SH

word2vec 真是神器啊，这篇文章终于又引爆了icml2014。nlp toolkits for personality and humanity！！！
@清华自然语言处理实验室
ICML2014看点：Distributed Representations of Sentences and Documents。继word2vec大火之后，Quoc Le和Tomas Mikolov将向量表示从词汇推进到了文档级别，值得关注。 #ICML2014Keywords# O网页链接

many neural language models， 真是意气风发！！！ 期待小型创业公司的伟大产品出现！
@清华自然语言处理实验室
ICML2014看点：Multimodal Neural Language Models。基于神经网络的语言模型近年来备受追捧，而多模态学习也是近年来的热点（ACL2013最佳论文即为此方向研究），这篇文章同时占了这两个吸引眼球的主题。 #ICML2014Keywords# O网页链接

产品制胜，product-driven not technology-driven 当然，技术可行性也很重要。关注google和microsoft的历史论文，挖掘小公司创业的可能性。
@张栋_机器学习
在 ICML 听到很多有趣事情：最早 Deep Learning 应用在语音识别是微软研究院几个实习生做出来的，发表文章。Google 看到后，做出了产品。微软看到 Google 把产品做出来了，再组织开发产品 ... 其实：第一个科研成果的人很伟大，第一个把科学成果应用在产品上，并且变成规模化大众用户产品的，更伟大！

强强联合，大牛云集。不过，还是有点不理解，为啥有些论文会有这么多牛人在。
@丁珰2008
Building high-level features using large scale unsupervised learning，Quoc Le, Marc'Aurelio Ranzato, Rajat Monga, Matthieu Devin, Kai Chen, Greg Corrado, Jeff Dean, Andrew Ng。看到这个作者列表，我和我的小伙伴们都惊呆了[ppb鼓掌]

华人的技术圈子进步很快，必须跟上大家的节奏le!!!
@星空下的巫师
TAPMI迎来新的Associate Editors： Hiroshi Ishikawa, Rong Jin, Hugo Larochelle, Fei-Fei Li, Yael Moses, Tobias Scheffer, Charles Sutton, Ben Taskar, Huan Xu, and Jieping Ye，多了好几位华人学者啊。。。

2014-6-23

Yann LeCun energy-based learning
@赵家平USC
读了Yann 50页的EBMs: a tutorial on energy-based learning, 受益匪浅：graphical model只是EBM在loss function是negative log-likelihood时的特例；著名的max-margin markov nets, CRF, SVMM都可以统一在EBM框架下，只是各自loss function不同；learning其实为energy surface adjustment过程[good]

semantic analysis is the next point that we must need to solve in mobile times!
@王威廉
看了一下今年ACL 2014语义分析研讨会的阵容，非常华丽: Kevin Knight, Percy Liang, Raymond Mooney, Hoifung Poon, Mark Steedman, Stefanie Tellex, Luke Zettlemoyer。录取论文：O网页链接

2014-6-24

acl2014 Don't count, predict! A systematic comparison of context-counting vs. context-predicting semantic vectors 总感觉acl的文章比icml的水分大很多，进展也更缓慢！
@李明辉_雕侠_nlp
词向量又有新名字了，context predict model，与此对应，传统方法称为count model 221202

deep learning 会让 semantic analysis 向前跑两步，大家都很期待！今天icml的热点就是明天工业界的必备工具。 //@李航博士:搜索技术发展到今天，相关性（也就是搜的结果要准）方面，我们觉得有两块比较重要，排序学习（learning to rank）和语义匹配（semantic matching）。在这个小册子里，我们将近
@李航博士
做个广告。我和徐君博士的书《Semantic Matching in Search》最近出版了。O网页链接 O网页链接

deep learning for nlp，很好的地方！ //@鲁东东胖:顺便做个广告, 我们(Noah's Ark Lab@ Hong Kong)在做deep learning on natural language processing的研究,有兴趣做intern同学可以和我私信联系, 可以趁着开会的时间聊一聊 //@高斌MS: 微软亚洲研究院曹涌研究员和华为诺亚方舟实验室吕正东研究员还将
@高斌MS
国际机器学习大会ICML 2014马上将在北京举行，我们在会上组织了Workshop on Knowledge-Powered Deep Learning for Text Mining，蒙特利尔大学Yoshua Bengio教授和微软亚洲研究院常务副院长马维英博士将分别做主题报告，欢迎参加！时间：6月26日。地点：北京国际会议中心。O网页链接

一定要善于利用个人和群体的智慧，当然这需要优秀的设计，对社会关系和人性以及生活意义的深刻洞察。
@鲍捷AI
Memect是一家做什么的公司？它致力于把认知剩余流动起来，把千千万万的人的头脑关联起来，变成一个虚拟的智能计算引擎。价值在流动中被创造，公司的使命就是创造一个信息流动摩擦力尽可能小的高速渠道

有些东西，你终究会相信，只是时间问题，或者你不愿去面对。deep learning会带来的变化还有很多，当然我们需要更宽更深的世界观，这只是一个Tipping Point。旧势力慢慢老去，新生力量正快速走向舞台的中心。
@褚达晨
比肉眼更狠的DL：人脸识别新技术准确率超99% O比肉眼更狠！人脸识别新技术准确率超99%

http://bbs.iheima.com/forum.php?mod=viewthread&tid=42947 互联网公司巅峰期过后维稳问题：身处困境的Twitter如何自救？ 《连线》杂志发表文章称，Twitter已身处困境，市值瞬间缩水，员工和投资人纷纷抛售股票，盛极一时的Twitter正在褪去昔日的光环。接下来，Twitter若想走出困境，避免步美国在线AOL的后尘，那么。。。真是一波接一波啊

watson或siri类系统，对问题理解和对话模式处理上，还有很多工作要做啊！希望semantic 方面的问题在今后2年有更大的突破。自己没机会读博，希望Socher、Goodfellow等几位一直关注的phd毕业时能给大家带来一些好东西。 //@昊奋:如果对应到IBM的watson系统上，grounding就是确定LAT (lexical answer type
@李志飞AI
做一个通用的semantic parser是不是一个伪命题？因为涉及到semantic的东西都很application-specific，既然这样就很难做成通用，对吧？比如说对下面这个句子通用的semantic该怎么表示：“明天我想坐飞机去北京，从上海出发，下午3点后走，最好是南航的”？@刘洋THU @52nlp @刘群MT-to-Death @孙乐_ISCAS

大家一起来造锤子吧，集体智慧，终有一个能成功。
@骆逸
想造一个类似IBM Watson的自然语言问答服务吗？来看看开源项目Quepy O网页链接 。Quepy提供了一个将自然语言查询转化为知识库查询的开发框架，目前支持Sparql和MQL两种查询语言，可以直接应用于DBpedia和Freebase。Quepy使用Python作为编程语言。CC @老淘 @西瓜大丸子汤 @python4cn

期待watson系统的各位research scientists and development engineers 能给大家带来更多新东西，如果有什么开源工具就更好了。 //@BoxingChen:右边是IBM Watson的研究员Fei Huang，做NLP，MT和ML的赶紧关注啊。[呵呵] //@黄非_巴別塔下添砖忙: 有点喜欢sofia的味道了，虽然有些陈旧 却没有那麽多喧嚣吵
@陈博兴-NLP
会议结束后，一个人在索菲亚市中心的老城区做了5个小时的随机游走，尽量避开景点和游客。转了转老街道，逛了逛了旧书摊和菜市场。夕阳下，人们悠闲地坐在街心公园和路边吃着冰淇淋和喝着啤酒。走在由石块铺成的窄窄的街道上，有一种久违的在欧洲的感觉。于是对这个城市多了几分喜欢。3星半推荐[嘻嘻]

http://oaqa.github.io/ oaqa Open Advancement of Question Answering Systems

The Watson question answering system developed at IBM research is the first highly-visible example of what is possible with this approach.
@tony的微博
O网页链接 oaqa Open Advancement of Question Answering Systems

The OAQA approach is the foundation for many sponsored research and development projects in the Language Technologies Institute at CMU, not only for question answering but also for related language applications such as Multimedia Event Detection. //@tony的微博:The Watson question
@tony的微博
O网页链接 oaqa Open Advancement of Question Answering Systems

http://www.cs.cmu.edu/afs/cs/Web/People/nico/pubs.html Nico Schlaefer My research at Carnegie Mellon was supported by IBM Ph.D. Fellowships from 2009 to 2011. phd thesis Nico Schlaefer: Statistical Source Expansion for Question Answering. Ph.D. Thesis, 2012.

For my work on question answering systems and contributions to the IBM Watson system, I received CMU's Allen Newell Award for Research Excellence (with Eric Nyberg, Teruko Mitamura, and Hideki Shima) in 2012.
@tony的微博
O网页链接 Nico Schlaefer My research at Carnegie Mellon was supported by IBM Ph.D. Fellowships from 2009 to 2011. phd thesis Nico Schlaefer: Statistical Source Expansion for Question Answering. Ph.D. Thesis, 2012.

watson系统核心researcher，可以好好学习一下。DeepAQ //@tony的微博:For my work on question answering systems and contributions to the IBM Watson system, I received CMU's Allen Newell Award for Research Excellence (with Eric Nyberg, Teruko Mitamura, and Hideki Shima) in 2012.
@tony的微博
O网页链接 Nico Schlaefer My research at Carnegie Mellon was supported by IBM Ph.D. Fellowships from 2009 to 2011. phd thesis Nico Schlaefer: Statistical Source Expansion for Question Answering. Ph.D. Thesis, 2012.


