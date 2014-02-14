---
layout: cn_post
title: 中文编码
categories: [编程]
tags: [中文, 编码]
---

    #coding=utf-8


    defis_chinese(uchar): 

    '''''判断一个unicode是否是汉字'''

    ifuchar >= u'\u4e00'anduchar<=u'\u9fa5': 

    returnTrue

    returnFalse

    defis_number(uchar): 

    """判断一个unicode是否是数字"""

    ifuchar >= u'\u0030'anduchar<=u'\u0039': 

    returnTrue

    returnFalse

    defis_alphabet(uchar): 

    """判断一个unicode是否是英文字母"""

    if(uchar >= u'\u0041'anduchar<=u'\u005a') \ 

    or(uchar >= u'\u0061'anduchar<=u'\u007a'): 

    returnTrue

    returnFalse


