---
layout: cn_post
title: darts 优化dat实现
categories: [编程]
tags: [dat, 双数组]
---

Darts(Double-ARray Trie System) 是日本的 Taku kudo (也是 CRF++ 
的作者) 实现的一个双数组， 接口简单，只提供了一个约 500 行代码
的头文件 darts.h,  实现的逻辑也相对简单， 如果了解双数组的原理
的话，要读懂代码并不难。目前两个著名的开源日文分词系统 Mecab, 
Chasen 都使用 Darts 构建词典， 检索速度快， 但是有点浪费内存。


