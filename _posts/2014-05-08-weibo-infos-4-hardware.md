---
layout: cn_post
title: 2014reading weibo信息轨迹4 hardware
categories: [生活]
tags: [weibo]
---

2014-5-8

最近看了几篇Facebook的engineer blog，谈到不少现代计算机体系结构下的程序优化问题。其实和spark以及graphlab等的流行，都源于多核CPU和大量内存的出现。现在单机16-60个core的CPU和64gb-1tb的内存很常见。

最近wordpress屏蔽很严重，用一下立马下线，反而Facebook比以前好用了一些。

ssd是新时代的一大利器，加上更好的随机读写算法，graphchi获得了很好的单机性能。sandisk刚刚发布4tb的企业级ssd，明年8tb后年16tb，新时代已经完全到来。扔掉那些古董恐龙工具，迎接新一代的软硬件工具链。

关于大内存，三星最近也发布了单条32gb的ddr4内存，2133mhz，新一代的服务器马上就要出来了。买2台做个人数据中心，真正的个人计算时代已经来临。

一年前自己的理想单机服务器，2*8core的CPU，24*16gb=400gb内存，4*4tb硬盘。最近都刷新了，4*15core的cpu，48*64gb=3tb的ddr4内存，4*8tb的ssd。神器!

http://tonyskywalker.github.io/2014/03/25/bigdata-traps-2-server-in-future/ 几个月前的理想服务器，最近ssd的发展可以说是突飞猛进，希望其他系统尤其是CPU的性能和内存的价格也能有更大突破。

Tom Rosamilia指出POWER8的创新不止是速度快50%，而是82倍！沃森系统最初运行在Power7上，而今天沃森运行在POWER8上能力提升5倍以上，吞吐量达到2倍以上。考虑到能耗、管理、空间的节省都是一个替代——这就是今天发布的新一代IBM Power系统，四年投入24亿美元，构建POWER8的基础。

一直期待watson系统相关的工具链发展，现在openpower对cpu的发展很值得想象。 尤其是有google的支持和一批跟风者。

中国工程院院士倪光南表示：我国重要行业中大量采用外国跨国公司的软硬件，号称“八大金刚”盘距中国重要行业，即思科(Cisco)、IBM、谷歌(Google)、高通(Qualcomm)、英特尔(Intel)、苹果(Apple)、Oracle(甲骨文)和微软(Microsoft)，它们在“棱镜门”事件中起到重要作用。要保障国家信息安全必须去除。

从去IOE到SOA我们只看到IBM，Oracle，EMC，SAP和埃森哲，这回又出来个八大金刚，饭得一口口吃，去皮剥肉也要一点点来，更何况去除八大金刚，这可真是一项艰巨和长期的任务，比八年抗战要难很多。

去ioe，去soa，对某些来说是口号，另一些是大势所趋。最终的设计原则是一样的， 技术有自己的进化规律。kiss for humanity！庆幸自己一开始就反对某些恐龙工具， 给大脑留了不少存储空间，做其他更值得期待的事情。

NVIDIA(英伟达)发布由NVIDIA、IBM共同研发的NVLink高速互连技术，可以加速GPU和CPU的通信，IBM Power等处理器将对其进行支持。与Mellanox的GPUDirect技术相比，NVLink解决了机器内的带宽瓶颈，而GPUDirect则让GPU可以高速和另一台服务器的GPU进行通信。

NVIDIA与Mellanox同为OpenPower联盟成员，据悉，NVLink的带宽能够达到现在PCIe 3.0总线速度的5-12倍。足以媲美CPU的内存带宽，可以让CPU-GPU、GPU-GPU更快地互相沟通。

gpu现在的发展飞快，尤其是memory的限制和cpu的通信问题。对机器学习的计算难题给予很大支持，这几年会有更多人进入。关键在于价格问题。希望各项工具之间的相互影响，共同进步。期待未来的personal computing。

http://www.aaronsw.com/2002/html2text/ Convert HTML to Markdown-formatted text https://github.com/aaronsw/html2text aaronsw

2014-5-9

http://cs.stanford.edu/~pliang/papers/ percy liang

http://www.cs.toronto.edu/~amnih/ https://tspace.library.utoronto.ca/bitstream/1807/24832/3/Mnih_Andriy_201006_PhD_thesis.pdf andriy mnil

http://umontreal.academia.edu/JosephTurian joseph turian paper

2014-5-10

Datastax带领着Cassandra的研发，Databricks带领着Spark的研发。今天Databricks宣布了Datastax的合作计划增进Spark和Cassandra两个生态圈的结合。这代表Spark会跨出传统的Hadoop生态圈，走向在线数据分析，也代表着Cassandra的用户未来可以得到更强大的数据分析功能。

关注大数据背景下的知识挖掘：华盛顿大学的第四代Open IE项目 http://knowitall.github.io/openie/ 前三代分别对应的项目是 Ollie (EMNLP 2012) Reverb (EMNLP 2011) TextRunner (IJCAI 2007)。

http://ijcai.org/papers13/contents.php ijcai2013 papes

北京的ICML 2014，深圳的ICDM 2014，上海的CIKM 2014，杭州的VLDB 2014，北京的ACL 2015。中国学术从cs开始崛起！

http://www.cikm2013.org/accepted.php cikm2013 papers acm的会议论文什么时候open access就好了。

http://www.wsdm-conference.org/2014/accepted-papers/ wsdm2014 papers

http://www.cs.uvm.edu/~icdm/  icdm

http://openreview.net/ http://openreview.net/venue/iclr2013 iclr2013 (International Conference on Learning Representations) papers

http://hltdays.ipipan.waw.pl/node/51 human language technology 2012 The Knowledge Graph, Information Extraction and Text Summarization at Google

http://www.akbc.ws/2014/ AKBC 2013 Automated Knowledge Base Construction (AKBC) 2013

2014-5-11

http://highscalability.com/blog/2014/3/31/how-whatsapp-grew-to-nearly-500-million-users-11000-cores-an.html How WhatsApp Grew to Nearly 500 Million Users, 11,000 cores, and 70 Million Messages a Second

看见Amazon云计算业务的创始人都来自Microsoft，你怎么想？看见SAP五位创始人都来自IBM你怎么想？看见Salesforce创人来自Oracle你怎么想？WhatsApp创始人来自Yahoo你又能这么想？

http://highscalability.com/blog/2011/12/6/instagram-architecture-14-million-users-terabytes-of-photos.html Instagram Architecture: 14 Million users, Terabytes of Photos, 100s of Instances, Dozens of Technologies

http://highscalability.com/blog/2014/2/26/the-whatsapp-architecture-facebook-bought-for-19-billion.html The WhatsApp Architecture Facebook Bought For $19 Billion

http://highscalability.com/blog/2013/4/15/scaling-pinterest-from-0-to-10s-of-billions-of-page-views-a.html Scaling Pinterest - From 0 to 10s of Billions of Page Views a Month in Two Years

http://highscalability.com/blog/2012/4/16/instagram-architecture-update-whats-new-with-instagram.html Instagram Architecture Update: What’s new with Instagram?

http://makerhacker.github.io/paper-mining/acl/home/acl2013_home.html acl2013 paper mining knowledge graph about tfidf lsi lda

http://makerhacker.github.io/paper-mining/acl/home/acl2010_home.html acl2010 paper mining knowledge graph about tfidf lsi lda

http://makerhacker.github.io/paper-mining/nips/home/nips2013_home.html nips2013 paper mining knowledge graph about tfidf lsi lda

http://makerhacker.github.io/paper-mining/nips/home/nips2010_home.html nips2010 paper mining knowledge graph about tfidf lsi lda

WEBDICT词库计划-免费无版权的互联网词库更新：从1GB果壳语料、750MB豆瓣语料、2GB腾讯新闻语料、2.5GB腾讯财经语料、500MB腾讯科技语料中增加词语19739个，剩余候选词已上传至主页 http://webdict.info/ 等候标注，详情在 https://github.com/ling0322/webdict。

