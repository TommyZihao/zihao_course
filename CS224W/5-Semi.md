# 半监督节点分类：标签传播和消息传递

> 同济子豪兄 2023-2-9
>

## 视频

中文精讲视频：https://www.bilibili.com/video/BV1184y1G7pA

Youtube视频：

https://www.youtube.com/watch?v=6g9vtxUmfwM&list=PLoROMvodv4rPLKxIpqhjhPgdQy7imNkDn&index=14

https://www.youtube.com/watch?v=QUO-HQ44EDc&list=PLoROMvodv4rPLKxIpqhjhPgdQy7imNkDn&index=15

https://www.youtube.com/watch?v=kh3I_UTtUOo&list=PLoROMvodv4rPLKxIpqhjhPgdQy7imNkDn&index=16

## 本讲介绍

斯坦福大学CS224W图机器学习公开课-同济子豪兄中文精讲

课程大纲、中文笔记课件、论文笔记、代码、思考题、扩展阅读、答疑群：https://github.com/TommyZihao/zihao_course/tree/main/CS224W

本讲总结了半监督节点分类问题的常见解决方法：特征工程、图嵌入表示学习、标签传播、图神经网络。
基于“物以类聚，人以群分”的Homophily假设，讲解了Label Propagation、Relational Classification（标签传播）、Iterative Classification、Correct & Smooth（C & S）、Loopy Belief Propagation（消息传递）、Masked Lable Prediction等半监督和自监督节点分类方法。

这些方法经常被用于节点分类任务的Baseline比较基线。消息传递和聚合的思路也影响了后续图神经网络的设计。

关键词：Message Passing, Label Propagation, Collective Classification, Self-supervised Learning

## 半监督节点分类问题-求解方法对比


| 方法               | 图嵌入 | 表示学习 | 使用属性特征 | 使用标注 | 直推式 | 归纳式 |
| ------------------ | ------ | -------- | ------------ | -------- | ------ | ------ |
| 人工特征工程       | 是     | 否       | 否           | 否       | /      | /      |
| 基于随机游走的方法 | 是     | 是       | 否           | 否       | 是     | 否     |
| 基于矩阵分解的方法 | 是     | 是       | 否           | 否       | 是     | 否     |
| 标签传播           | 否     | 否       | 是/否        | 是       | 是     | 否     |
| 图神经网络         | 是     | 是       | 是           | 是       | 是     | 是     |

- 人工特征工程：节点重要度、集群系数、Graphlet等。

- 基于随机游走的方法，构造自监督表示学习任务实现图嵌入。无法泛化到新节点。

  例如：DeepWalk、Node2Vec、LINE、SDNE等。

- 标签传播：假设“物以类聚，人以群分”，利用邻域节点类别猜测当前节点类别。无法泛化到新节点。

  例如：Label Propagation、Iterative Classification、Belief Propagation、Correct & Smooth等。

- 图神经网络：利用深度学习和神经网络，构造邻域节点信息聚合计算图，实现节点嵌入和类别预测。

  可泛化到新节点。

  例如：GCN、GraphSAGE、GAT、GIN等。

## 思考题

哪些图数据挖掘问题，可以抽象成半监督节点分类问题？

有哪些解决半监督节点分类问题的方法？各有什么特点？（对照表格简述）

如何理解Transductive Learning（直推式学习）？

如何理解Inductive Learning（归纳式学习）？

本讲讲了哪些标签传播和集体分类方法？

如何理解网络中的Homophily？

简述Label Propagation的算法原理。

Label Propagation是否用到了节点的属性特征？

简述Iterative Classification的算法原理。

Iterative Classification如何使用节点之间的关联信息？

为什么Relational Classification和Iterative Classification都不保证收敛？

简述C & S的基本原理

如何计算Normalized Adjacency Matrix？

如何用图论解释成语“三人成虎”、“众口铄金”？

如何用图论解释《三体》中的“猜疑链”？

简述Loopy Belief Propagation的基本原理。

简述Masked Label Prediction的基本原理。

Masked Label Prediction可以是Inductive的吗？可以泛化到新来的节点吗？

本讲的方法，与图神经网络相比，有何异同和优劣？

如何重新理解“出淤泥而不染”？

如何重新理解“传销”、“病毒式裂变”？

## 线性代数知识补充

当且仅当矩阵谱半径严格小于1，矩阵乘幂收敛。

> 谱半径指最大奇异值的模长。
>
> 对称矩阵、非对称矩阵中的可对角化矩阵：最大奇异值就是最大特征值的平方，奇异值和特征值一一对应。
> 非对称矩阵，不可对角化矩阵：不便讨论

## 特别感谢

赵冰辰（爱丁堡大学）

耿珺（斯坦福大学）

