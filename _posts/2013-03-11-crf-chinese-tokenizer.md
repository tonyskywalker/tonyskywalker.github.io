---
layout: cn_post
title: crf 中文分词
categories: [语言]
tags: [语言, crf, 中文, 分词]
---

CRF

中文分词是互联网应用不可缺少的基础技术之一，也是其他语音和语言产品必不可少的技术组件。

自2003年第一届国际中文分词评测以来，由字构词的分词方法获得了压倒性优势，国内主要通过CRF++开源软件包来学习该分词方法，但是CRF++过于复杂的代码结构，导致了该算法的普及率。

CRF中文分词开源版仅仅包含CRF++软件包中分词解码器部分，简化了CRF++复杂代码结构，清除了分词解码器不需要的代码，大大提高了分词解码器的可读性和可懂度。同时为了方便学习者可视化跟踪和调试代码，在Windows平台下分别建立了VC6.0和VS2008两个工程文件，使得VC6.0用户和VS2008用户都能轻玩转中文分词。



