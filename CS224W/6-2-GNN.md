# 图神经网络综述和学习路径

> 同济子豪兄 2023-3-7
>

## 视频

中文精讲视频：https://www.bilibili.com/video/BV16v4y1b7x7

Youtube视频：https://www.youtube.com/watch?v=MH4yvtgAR-4&list=PLoROMvodv4rPLKxIpqhjhPgdQy7imNkDn&index=19

## 本讲介绍

斯坦福大学CS224W图机器学习公开课-同济子豪兄中文精讲

课程大纲、中文笔记课件、论文笔记、代码、思考题、扩展阅读、答疑群：https://github.com/TommyZihao/zihao_course/tree/main/CS224W

本讲是图神经网络基础课，先介绍了图机器学习、图深度学习、表示学习、图嵌入等基础概念，引出图神经网络在各类图机器学习任务的应用场景，及其研究领域综述和学习路径。

在图数据上运行深度学习算法，会遇到诸多难点和挑战：参数量（过拟合）问题、归纳泛化问题、顺序不变问题、过平滑问题等。

以图卷积神经网络GCN为例，介绍了消息传递计算图的构建方式、邻域特征聚合函数、GNN层数计算等基本概念。

关键词：

Machine Learning, Deep Learning, Graph Neural Networks, GNN, Graph Convolutional Neural Networks, GCN, Knowledge Graph

## 扩展阅读

李沐老师推荐的GNN博客1：https://distill.pub/2021/gnn-intro

李沐老师推荐的GNN博客2：https://distill.pub/2021/understanding-gnns

Paperswithcode图任务：https://paperswithcode.com/area/graphs

Cora节点分类数据集上的比分：https://paperswithcode.com/sota/node-classification-on-cora

DIFFPOOL论文：https://arxiv.org/pdf/1806.08804.pdf

《图神经网络 基础、前沿与应用》人民邮电出版社 异步图书社区，部分章节电子版

https://graph-neural-networks.github.io

五折购书（正版全新）：公众号 人工智能小技巧 回复 城堡书

## 思考题

什么是图机器学习？什么是图表示学习？什么是图嵌入？什么是图深度学习？

图神经网络本质上在解决什么问题？

图神经网络可以解决哪些图机器学习任务？这些任务都有哪些Benchmark？

图神经网络包含哪些研究领域？可以和哪些人工智能研究方向交叉？

什么是图转换？图匹配？图结构学习？

为什么不能把邻接矩阵直接输入到神经网络中？

为什么不能把图直接输入到卷积神经网络中？

什么是消息传递图神经网络？

如何理解“顺序不变性”和“顺序等变性”？

## 特别感谢

赵冰辰（爱丁堡大学）、李沐（亚马逊）、张军斌（图科学实验室）