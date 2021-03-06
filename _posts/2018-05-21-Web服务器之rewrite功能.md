---
layout:     post
title:      Web服务器之rewrite功能
subtitle:   
date:       2018-05-21
author:     挨踢灰太狼
header-img: img/post-bg-os-metro.jpg
catalog: true
tags:
    - web
---

# 概念 

URL Rewrite即URL重写，就是把传入Web的请求重定向到其他URL的过程。

# 为什么web服务器需要rewrite功能呢？ 

**1.首先是满足观感的要求。**
对于追求完美主义的网站设计师，就算是网页的地址也希望看起来尽量简洁明快。形如http://www.123.com/news/index.asp?id=123的网页地址，自然是毫无美感可言，而用UrlRewrite技术，你可以轻松把它显示为 http://www.123.com/news/123.html。

**2.其次可以隐藏网站所用的编程语言，还可以提高网站的可移植性。**
当网站每个页面都挂着鲜明的.asp/.aspx/.php这种开发语言的标记，别人一眼即可看出你的网站是用什么语言做的。而且在改变网站的语言的时候，你需要改动大量的链接。而且，当一个页面修改了扩展名，它的pagerank也会随之消失，从头开始。我们可以用UrlRewrite技术隐藏我们的实现细节，这样修改移植都很方便，而且完全不损失pagerank。提高安全性，可以有效的避免一些参数名、ID等完全暴露在用户面前，如果用户随便乱输的话，不符合规则的话直接会返回个404或错误页面，这比直接返回500或一大堆服务器错误信息要好的多

**3.最后也是最重要的作用，是有利于搜索引擎更好地抓取你网站的内容。**
理论上，搜索引擎更喜欢静态页面形式的网页，搜索引擎对静态页面的评分一般要高于动态页面。所以，UrlRewrite可以让我们网站的网页更容易被搜索引擎所收录。

转自： https://blog.csdn.net/shimiso/article/details/8594885


