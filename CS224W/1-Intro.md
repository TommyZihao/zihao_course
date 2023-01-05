# 图机器学习导论

> 同济子豪兄 2023-1-3

同济子豪兄-中文精讲视频：https://www.bilibili.com/video/BV1pR4y1S7GA

本讲介绍了图数据挖掘的常见任务、典型方法、应用场景、编程工具。图是描述大自然各种关联现象的通用语言，图无处不在。不同于传统数据分析中样本独立同分布假设，图数据自带了关联结构，需要使用专门的图神经网络进行深度学习。
本讲介绍了斯坦福CS224W公开课的课程大纲；在节点、连接、子图、全图各个层面进行图数据挖掘的典型任务，以及在蛋白质结构预测、生物医药、内容推荐、文献挖掘、社交网络、开源项目评价等领域的应用。

## 官方原版视频

Youtube视频：

https://www.youtube.com/watch?v=JAB_plj2rbA&list=PLoROMvodv4rPLKxIpqhjhPgdQy7imNkDn&index=1

https://www.youtube.com/watch?v=JAB_plj2rbA&list=PLoROMvodv4rPLKxIpqhjhPgdQy7imNkDn&index=2

## 课程主页

https://web.stanford.edu/class/cs224w

Graph Representation Learning Book：https://www.cs.mcgill.ca/~wlh/grl_book/

 Lecture 1.1 - Why Graphs：https://www.youtube.com/watch?v=JAB_plj2rbA&list=PLoROMvodv4rPLKxIpqhjhPgdQy7imNkDn&index=1

## Jure Leskovec

个人主页：https://cs.stanford.edu/people/jure/

谷歌学术主页：https://scholar.google.com/citations?user=Q_kKkIUAAAAJ&hl=zh-CN

## 图机器学习编程工具

PyG：www.pyg.org

NetworkX：networkx.org

DGL：www.dgl.ai

AntV图可视化工具Graphin：graphin.antv.vision

AntV图可视化工具G6：g6.antv.antgroup.com

Echarts可视化：echarts.apache.org/examples/zh/index.html#chart-type-graphGL

## AlphaFold

AlphaFold官网：https://www.deepmind.com/research/highlighted-research/alphafold

AlphaFold蛋白质数据库：https://alphafold.ebi.ac.uk

AlphaFold博客1：https://www.deepmind.com/blog/alphafold-using-ai-for-scientific-discovery-2020

AlphaFold博客2：https://www.deepmind.com/blog/alphafold-reveals-the-structure-of-the-protein-universe

AlphaFold自然杂志论文：https://www.nature.com/articles/s41586-019-1923-7.epdf?author_access_token=Z_KaZKDqtKzbE7Wd5HtwI9RgN0jAjWel9jnR3ZoTv0MCcgAwHMgRx9mvLjNQdB2TlQQaa7l420UCtGo8vYQ39gg8lFWR9mAZtvsN_1PrccXfIbc6e-tGSgazNL_XdtQzn1PHfy21qdcxV7Pw-k3htw%3D%3D

AlphaFold代码：https://github.com/deepmind/deepmind-research/tree/master/alphafold_casp13

百度文心·生物计算大模型：https://wenxin.baidu.com/wenxin/paddlehelix

人工智能在药物发现和生物技术中的应用：2022年回顾与关键趋势：https://mp.weixin.qq.com/s/ZuDpd2YqHpDiRqw9GIXolw

## 思考题

打开你的手机，里面那些APP用到了图机器学习和图神经网络的技术？（内容个性化推荐、社交网络、银行金融）

A股、港股、美股市值最高的上市公司，哪些公司的核心资产是图？

观看电影《社交网络》，图和图数据挖掘的商业价值体现在哪些方面？

马化腾在2022年12月内部讲话提到，微信视频号是整个腾讯的希望，请从图的角度解释这句话。

在你自己的研究领域，哪些数据可以用图或者网络来表示，如何进行图数据挖掘？

近年来，图数据挖掘在哪些领域带来了革命性进展？

图数据挖掘解决哪些基本任务？

分别从图、连接、节点三个层面，举例解释图数据挖掘在生物医学方面的应用。

图神经网络为什么是端到端的？为什么不需要人工做特征工程？

图神经网络和其它神经网络有什么区别？

简述AlphaFold的基本原理，它解决了哪些以前解决不了的问题？

图机器学习和传统机器学习有什么区别和难点？

图机器学习的编程工具有哪些？看看它们的官网吧（Graphgym、pyG、networkx、dgl、Pytorch、AntV、Echarts）

## 其它阅读材料

李笑来-惊喜与创造惊喜的方法论：https://zhuanlan.zhihu.com/p/475615463

乔布斯在斯坦福大学毕业典礼的演讲：https://www.bilibili.com/video/BV1oW411h7Ea

子豪兄1024脱口秀-乔布斯传奇：https://www.bilibili.com/video/BV1Zf4y1g78Q

哥尼斯堡七桥问题：https://zhuanlan.zhihu.com/p/519123688

2022 IDEA大会｜BIOS V2正式发布，数据驱动构建超级医学知识图谱：https://mp.weixin.qq.com/s/vuHGUtWbiIH-pJ6MZaxl5Q

# 图的基本表示

同济子豪兄-中文精讲视频：https://www.bilibili.com/video/BV1n84y1e7SF

斯坦福原版视频：https://www.youtube.com/watch?v=P-m1Qv6-8cI&list=PLoROMvodv4rPLKxIpqhjhPgdQy7imNkDn&index=3

## 扩展阅读
如何解释人际交往中的「六度空间」理论，它是如何证明的？：https://www.zhihu.com/question/27492995/answer/37841402

## 思考题

举几个Heherogeneous Graph（异质图）的例子

异质图和普通图有什么区别？

举几个Bipartite Graph（二分图）的例子

举几个有向图的例子

如何设计本体图Ontology？

为什么要把图表示成矩阵？

如何从连通域的角度，理解“六度空间”理论：世界上任意两个人，可以通过不超过六个中间人，相互认识。

为什么很多真实场景的图都是稀疏的？
