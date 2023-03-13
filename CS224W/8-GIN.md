# 图神经网络的表达能力

> 同济子豪兄 2023-3-13
>

## 视频

中文精讲视频：https://www.bilibili.com/video/BV1MT411Y7da

Youtube视频：

https://www.youtube.com/watch?v=5vMEgYbka0A&list=PLoROMvodv4rPLKxIpqhjhPgdQy7imNkDn&index=26

https://www.youtube.com/watch?v=B5y47gWt3co&list=PLoROMvodv4rPLKxIpqhjhPgdQy7imNkDn&index=27

## 本讲介绍

斯坦福大学CS224W图机器学习公开课-同济子豪兄中文精讲

课程大纲、中文笔记课件、论文笔记、代码、思考题、扩展阅读、答疑群：https://github.com/TommyZihao/zihao_course/tree/main/CS224W

本讲讨论了图神经网络的表达能力，分析了GCN、GraphSAGE等常见消息传递GNN的表达能力，“单射重集聚合函数”对表达能力非常重要。并介绍了消息传递图神经网络中表达能力最强的Graph Isomorphism Network(GIN)，通过神经网络拟合哈希函数，理论上能够达到Weisfeiler Lehman Kernel的效果。

GIN论文：How Powerful are Graph Neural Networks? ICLR2019

关键词：

Machine Learning, Deep Learning, Neural Networks, Graph Neural Networks, GNN, Graph Convolutional Neural Networks, GCN, GraphSAGE, Graph Attention Networks, GAT, Graph Isomorphism Network, GIN

## 扩展阅读

GIN论文：How Powerful are Graph Neural Networks?

https://arxiv.org/abs/1810.00826

## 思考题

不同类型的神经网络，表达能力各有何区别？

为什么要研究图神经网络的表达能力？

图神经网络的表达能力如何体现？

GCN的表达能力如何？

GraphSAGE的表达能力如何？

GAT的表达能力如何？

GIN的表达能力如何？

图神经网络的表达能力，关键取决于哪一步操作？

什么是函数的单射、满射、双射？

求和、最大池化、求平均，三者的表达能力如何排序？

和普通集合相比，“重集合”有什么特点？

消息传递图神经网络的表达能力上限是什么？

简述WL测试的基本原理

简述“万能近似定理”的内容，为什么它这么重要？

GIN和GCN的表达能力有什么区别？

如何在GIN的基础上，进一步提升GNN的表达能力？