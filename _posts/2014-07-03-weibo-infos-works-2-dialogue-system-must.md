---
layout: cn_post
title: 2014working weibo点滴记录2 dialogue system must
categories: [生活]
tags: [weibo]
---

2014-07-03

http://corner.squareup.com/2013/08/fly-vim-first-class.html The Corner Square Engineering Blog Fly Vim, First-Class August 28, 2013

Engineers at Square use a wide variety of code editors: Sublime, IntelliJ, Xcode, and Vim are among the most popular. Over time, the Square Vim enthusiasts have compiled settings, shortcuts, and plugins into a single repo we lovingly call Maximum Awesome, which we are open-sourci
@tony的微博
O网页链接 The Corner Square Engineering Blog Fly Vim, First-Class August 28, 2013

http://www.datacenterknowledge.com/archives/2014/06/03/facebook-testing-broadcoms-open-compute-switches-production/ Facebook Testing Broadcom’s Open Compute Switches in Production

It has been a year since Facebook announced that its Open Compute Project had an initiative focused on defining a network switch that could be used with a variety of operating systems, so that data center operators would not get locked into using a single vendor’s software once
@tony的微博
O网页链接 Facebook Testing Broadcom’s Open Compute Switches in Production

This allows it to optimize the whole system for its applications and to win on price from competition among vendors. It already uses its own servers and storage arrays, both available as open source designs through OCP, and network gear has been the remaining piece of the puzzle.
@tony的微博
O网页链接 Facebook Testing Broadcom’s Open Compute Switches in Production

software for everything！ //@戴文渊:强烈推荐！基于大数据技术的Software-Defined Network(SDN)，有可能会颠覆现有的网络解决方案。我们在小规模网络上初试成功，显著提升网络效率。这个项目目前已经是公司级别的项目，在公司最高决策层立项通过，下一阶段要找真实运营商网络试点啦 [嘻嘻]
@彦辉_士提反
#华为诺亚方舟实验室招聘#请大家帮忙推荐优秀的同学，所做工作是应用机器学习去解决通信网络中的问题，要求算法基础好且网络系统实现能力强，研究员和工程师都需要，可以选择在香港或者深圳入职。有兴趣可以私信我或者发email到yhgeng@gmail.com @戴文渊 @码农陈嘉 @Jianc说 @Kerrigen @卖尔斯文

deep + learning + computing + data for everything！
@赵家平USC
Deep Learning除了在IT中有广泛的应用， 还能用在哪些领域呢？ 一年前Sebastian Seung 用CNN重建了老鼠视网膜里的plexiform layer；昨天UCI的学者在nature上撰文说DL可用于发现 希格斯玻色子 等exotic particles, 比传统的方法更精确O网页链接 看来DL在高能物理学，神经学，医学中都有应用

2014-7-4

系统级的优化，还有很多事情要做吧，尤其是移动智能计算时代！
@bnu_chenshuo
C1000k新思路：今年BSDCan14上有人把FreeBSD 9的TCP/IP协议栈移植到了用户态，意味着并发TCP连接不占用系统文件数，只占内存。优化也更直接，不再是调黑盒参数组合，而是直接上profiling，再改代码。用户态的吞吐量比不上内核，不过对C1000k应该不成问题。搜 libuinet。

2014-7-5

难得现在还有人在认真做底层基础系统优化！ //@何_登成:三晚阅读后的感觉：读懂这个系列的书，编写高性能程序，第一要素就是了解一些硬件，尤其是现阶段的主流CPU，毕竟程序是由CPU来执行的。庆幸本人从去年开始，就有意识的学习CPU的相关知识，因此现在阅读此书压力不算太大，希望以后能将书中的部分
@何_登成
推一个丹麦Copenhagen博士Agner Fog撰写的系列电子书：Optimization manuals O网页链接 作者有着深厚的编译器、CPU微处理器、C++语言功底，因此电子书也分为五篇，分别从C++/Compiler/Microprocessor等不同方面出发，阐述高性能程序设计需要掌握的知识。目前本人在看第一本，感觉非常不错！

2014-7-6

期待intel在cpu、memory等硬件系统平台工具链上做出更多有意思的事情！ //@老师木: //@keithcool: //@jiyifeng-nj: //@Taile梦呓:intel这步棋走的很高嘛。具有可编程能力的通用硬件+光互联，变成资源池，利用软件定义一切搞定大部分应用。背后的竞争的是工艺和生态系统。这个intel最擅长。以后基于fpga
@zolker
Intel数据中心总经理Diane Bryant在GigaOm Structure上宣布Xeon-FPGA混合处理器，已经开发了一年左右。Bryant说FPGA能带来几十倍的性能提升，去年已经制定了15种方案，一方面Facebook等公司也有定制化处理器的需求 另一方面对抗ARM，还是有点意思的 [哈哈] O网页链接

gcc -v Using built-in specs. Target: x86_64-linux-gnu Thread model: posix gcc version 4.4.7 (Ubuntu/Linaro 4.4.7-1ubuntu2)

clang -v Ubuntu clang version 3.0-6ubuntu3 (tags/RELEASE_30/final) (based on LLVM 3.0) Target: x86_64-pc-linux-gnu Thread model: posix
@tony的微博
gcc -v Using built-in specs. Target: x86_64-linux-gnu Thread model: posix gcc version 4.4.7 (Ubuntu/Linaro 4.4.7-1ubuntu2)

2014-7-8

大家都对这个应用爆发期很期待！热情很高啊！ //@余凯_西二旗民工:我觉得在感知，语言理解，知识表示，推理，规划，控制等方面，最近5年deep learning会使得感知perception有巨大进步，而语言理解LU有待突破，在控制方面reinformcement learning会有长足进展； 另外一方面，技术成熟是个过程，在不完美
@李志飞AI
实现AI需要听得懂（语音识别和自然语言理解），看得见（计算机视觉），走得动（Robotics），能思考和自我进化（推理）。还有别的吗？现在是每个子问题都非常难，你觉得近期内（如5年）哪个会有可能最先突破呢？ @余凯_西二旗民工

2014-7-9

应该会有很多公司跟着迁移吧！技术的变更总是能诞生很多coder的需求。
@郑昀
因为要摆脱Oracle对MySQL用户的潜在制约（如MySQL在5.5.30过渡到5.5.31版本期间逐渐闭源，不再公开补丁的测试数据和修订历史等），继苹果、维基百科等迁移数据库之后，Google高级系统工程师Jeremy Cole透露，谷歌的开源数据中心将由MySQL迁移至MariaDB，至此，Google的数据库已大部转向MariaDB10.0。

2014-7-10

https://mu.lti.cs.cmu.edu/trac/Ephyra/ Openephyra open source question answering systems by nico schlaefer from cmu

http://breakthroughanalysis.com/2013/03/04/all-about-natural-language-processing/ breakthroughanalysis.com All About Natural Language Processing and many interesting things！！！

http://www.cyc.com/platform/opencyc The OpenCyc Platform is your gateway to the full power of Cyc, the world's largest and most complete general knowledge base and commonsense reasoning engine. OpenCyc contains hundreds of thousands of Cyc terms organized in a carefully designed ontology.

Release 4.0 of OpenCyc includes: ◦The core Cyc ontology whose domain is all of human consensus reality. The current release includes: ◦~239,000 terms (up from ~177,000 terms in the previous release) ◦~2,093,000 triples (up from ~1,500,000 in the previous release)
@tony的微博
O网页链接 The OpenCyc Platform is your gateway to the full power of Cyc, the world's largest and most complete general knowledge base and commonsense reasoning engine. OpenCyc contains hundreds of thousands of Cyc terms organized in a carefully designed ontology.

看来大家都在热心研究word2vec和gensim啊！！！ //@梁斌penny:我没有按照标准做法，把1-hot数组通过随机矩阵搞绸密(文本图像化)，而是直接把文本看过是一个阶段的隐层直接搞，已经取得突破。。 //@李沐M:刚跟quoc吐槽，其实稀疏的文本数据搞稠密话后是处理简单很多，但其实很损失（分类）精度 //@西瓜
@西瓜大丸子汤
刚才说到python优化，举个具体的例子 Gensim的作者把word2vec(深度学习)做了几个经典优化：循环，numpy/BLAS，cython，多线程（真的可以）结果效率提高了上千倍，比Google开源出来的原始C版本还快3倍。他最近还写了个word2vec教程。无论是学习word2vec还是python优化，都不可不看 O网页链接

http://mp.weixin.qq.com/s?__biz=MzA3MjI2OTUxNQ==&mid=200374890&idx=1&sn=79154cac0b77112aa3f36d2b0609b552 【大数据100分】王昊奋：大规模知识图谱技术 看来国内厂商真正要在knowledge graph上发力了， 没想到weixin还有这种新闻！

用distributed representation for word and phase or paraphase and doc，可以做很多事情吧！不知道这里做分词是不是用了neural networks based language model？word2vec？
@梁斌penny
昨天，某大佬问我，深度学习在现有数据下有什么神奇之处。我回答，某博士完全不懂nlp，都做出分词了，这多神奇啊。

http://zhuanlan.zhihu.com/kstory/19652920 没想到zhihu上还有一小波作者，写一些精品文章。 语音、文字与思考方式 首先，文字让思考打破了时空的界限，让思考不必是连续不断，我们可以随时把以前记录下来的文字拿出来重新摆弄，当然现在有了录音技术，语音也可以跨时空了，但这只是最近的事。

其次，文字记录下来就是二维结构，而语音只是一维结构，这个多出来的维度让我们可以直接跳到文字中我们需要的部分，而语音即使我们录下来，要找到需要的那一段也只能在一维上快进快退，用过磁带录音机的朋友都有过倒带子找东西的经历。然后，文字呈现的是视觉符号，这样就可以借助人脑原本就具有的强大
@tony的微博
O知乎 没想到zhihu上还有一小波作者，写一些精品文章。 语音、文字与思考方式 首先，文字让思考打破了时空的界限，让思考不必是连续不断，我们可以随时把以前记录下来的文字拿出来重新摆弄，当然现在有了录音技术，语音也可以跨时空了，但这只是最近的事。

认真写blog，也是很珍贵的知识积累！个人也是人类的历史财富！ //@何_登成:个人博客，能在一个系列上不断深挖的不多。除此之外，另一个让我印象深刻的就是Jeff Preshing的博客：http://preshing.com/ 持续在并发编程上进行挖掘。我的大部分进阶并发编程知识，都是从Preshing的博客上获取的。好的系列博
@何_登成
推荐一个顶好的博客 http://codecapsule.com/ 作者Emmanuel来自Booking。内容包含两个系列的文章。系列一：Implementing a Key-Value Store http://codecapsule.com/2012/11/07/ikvs-implementing-a-key-value-store-table-of-contents/ 系列二：Coding for SSDs 博客写成书的质量，不得不赞。


