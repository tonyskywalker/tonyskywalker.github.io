---
layout: cn_post
title: 新词发现，词库整理
categories: [语言, 2013]
tags: [语言, 中文, 分词, 词库, 新词]
---

中文分词，词库整理主要解决三大问题：

1. 词频统计

2. 新词发现

3. 垃圾词过滤
 

下面的新词发现算法，可同时解决上面3个问题，保证词库质量。
 

挖掘新词的传统方法是，先对文本进行分词，然后猜测未能成功匹配的剩余片段就是新词。这似乎陷入了一个怪圈：分词的准确性本身就依赖于词库的完整性，如果词库中根本没有新词，我们又怎么能信任分词结果呢？此时，一种大胆的想法是，首先不依赖于任何已有的词库，仅仅根据词的共同特征，将一段大规模语料中可能成词的文本片段全部提取出来，不管它是新词还是旧词。然后，再把所有抽出来的词和已有词库进行比较，不就能找出新词了吗？

传统方法：

文本分词，已知词统计词频，同时用词频过滤掉垃圾词，未知词根据词频过滤发现新词。

问题是，分词的准确性依赖于词库的完整性。

新方法：

不考虑词库，从语料库中提取出可能的词语（n-gram），如果在现有词库中可用于统计词频，同时用词频过滤掉垃圾词；否则根据词频等特征过滤发现新词。

问题，提取可能的词语计算量较大，取n个字长的文本片段（n最大为5）。
 

判断是否成词的特征：

1. 词频：词出现的次数（文档数）/ 字的总数（文档总数），最好不要用文档数据。

2. 相关程度（词中汉字共同出现的概率）：

如果2者毫不相关，p(A.B) = p(A) . p(B)；否则p(A.B) > p(A) . p(B)，p(A.B)/p(A).p(B) 比值越大相关性越高。

如果遇到多个2个字的情况，需要考虑不同组合的概率，等于又做了一次分词计算。

ABC，要考虑A和BC，AB和C，A和B及C的情况，取比值最小者作为相关程度值。

3. 丰富程度（词在文本中运用的灵活程度）：

利用信息熵来衡量不确定性的大小，某个事件可能发生n种情况，p1，p2，p3，。。。pn。

信息熵 = p1.(-logp1) + p2.(-logp2) + p3.(-logp3) + ... + pn.(-logpn)。 

可以计算词在文本中左邻字集合和右邻字集合的信息熵，用于衡量该词在文本中自由运用的灵活程度。

 

我们把文本中出现过的所有长度不超过 d 的子串都当作潜在的词（即候选词，其中 d 为自己设定的候选词长度上限，我设定的值为 5 ），再为出现频数、相关程度和丰富程度各设定一个阈值，然后只需要提取出所有满足阈值要求的候选词即可。

使用2层循环，遍历文本，可以得到所有可能词语的特征信息

{% highlight c %}
class CandidateWord
{
const char *m_pText;

uint32_t m_num;

map<const char *, uint32_t> m_leftInfos;

map<const char *, uint32_t> m_rightInfos;
}
{% endhighlight %}

然后计算相关程度和丰富程度，设定过滤值，即可判断是否成词。

