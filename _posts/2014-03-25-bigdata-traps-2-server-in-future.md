---
layout: cn_post
title: 大数据的陷阱2 未来的服务器
categories: [互联网]
tags: [大数据]
---

目前谈大数据，和云计算有很大的关系，好像是个互联网公司都在做自己的私有云，搞分布式，搭建大数据分析平台。

但一般的公司需要这么庞大的系统集群吗？

1 没有这么多的计算量

2 管理太多的机器，复杂性太高，被机器所累

3 集群机器多了，网络成为瓶颈，性能反而下降

一般的互联网应用基本不会涉及复杂的计算，做一些机器学习和数据挖掘的项目，也不会涉及那么大的数据量。配置一些
高性能的PC服务器足以，开发部署和后期维护都会简单很多。

现在单台server的配置，3-5万这样已经很常见。
cpu：2cpu(8core) 16core
memory: 64GB-400GB
disk: 2hdd(2TB) or 4ssd(256GB)

按照现在的速度，3年后我们的理想服务器，5-10万做一些高级的应用。
cpu：4cpu(16core) 64-128core
memory: 1TB-10TB
disk: 2ssd(2TB)
network: 10GB
gpu：4gpu（20000core）

这样的机器，不论单机多核做并行处理，还是多级集群做分布式处理，如果加上spark和graphlab这样的高效框架，大数据的
计算和存储问题都不是很大。关键还是在于应用本身，对业务知识的理解，合适的模型和算法，高质量的数据和可爱的产品等等。

期待3年后的移动计算设备。
cpu：16-32core
memory：32GB-128GB（maybe）
disk：1-2TB
network：1-2GB
gpu: (1000core)

未来移动计算不是梦。

数据量的增加不是问题，关键在于个人数据的增加，模型更准确，应用更智能。



