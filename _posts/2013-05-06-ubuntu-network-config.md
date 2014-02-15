---
layout: cn_post
title: ubuntu网络配置
categories: [工具]
tags: [工具, ubuntu, 网络]
---

ubuntu

/etc/network/interfaces

1 #auto lo

2 #iface lo inet loopback

3 auto eth0

4 iface eth0 inet static

5 address 192.168.1.108

6 gateway 192.168.1.1

7 netmask 255.255.255.0

8 #network 192.168.3.0

9 #broadcast 192.168.3.255


