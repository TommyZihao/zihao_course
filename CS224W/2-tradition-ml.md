# 好的食材造就好的菜肴-传统图机器学习的特征工程

> 同济子豪兄 2023-1-10

同济子豪兄中文精讲视频：

节点特征工程：https://www.bilibili.com/video/BV1HK411175s

连接特征工程：https://www.bilibili.com/video/BV1r3411m7sD

全图特征工程：https://www.bilibili.com/video/BV14W4y1V7gg

斯坦福原版视频：

https://www.youtube.com/watch?v=3IS7UhNMQ3U&list=PLoROMvodv4rPLKxIpqhjhPgdQy7imNkDn&index=4

https://www.youtube.com/watch?v=4dVwlE9jYxY&list=PLoROMvodv4rPLKxIpqhjhPgdQy7imNkDn&index=5

https://www.youtube.com/watch?v=buzsHTa4Hgs&list=PLoROMvodv4rPLKxIpqhjhPgdQy7imNkDn&index=6

# 传统图机器学习方法-节点

## 扩展阅读

https://www.geeksforgeeks.org/eigenvector-centrality-centrality-measure

https://www.jsums.edu/nmeghanathan/files/2015/08/CSC641-Fall2015-Module-2-Centrality-Measures.pdf?x61976

https://aksakalli.github.io/2017/07/17/network-centrality-measures-and-their-visualization.html

上海地铁线路图：[http://www.shmetro.com](http://www.shmetro.com/)

上海地铁时刻表：http://service.shmetro.com/hcskb/index.htm

北京地铁线路图：[https://map.bjsubway.com](https://map.bjsubway.com/)

北京地铁时刻表：https://www.bjsubway.com/station/smcsj

https://hal.archives-ouvertes.fr/hal-01764253v2/document

NetworkX-常用图数据挖掘算法：https://networkx.org/documentation/stable/reference/algorithms/index.html

NetworkX-节点重要度算法：https://networkx.org/documentation/stable/reference/algorithms/centrality.html

NetworkX-Clustering算法：https://networkx.org/documentation/stable/reference/algorithms/clustering.html

NetworkX-最短路径算法：https://networkx.org/documentation/stable/reference/algorithms/shortest_paths.html

## 思考题

节点层面，存在哪些数据挖掘任务，有何应用场景？

“传统图机器学习方法”传统在何处？

特征工程在数据挖掘中有什么作用？

在传统图机器学习中，为什么要对节点、连接、全图做特征工程？

传统图机器学习方法相比图神经网络（深度学习），有什么优点和缺点？

节点层面可以构造哪些特征？这些特征可以归为哪两类？

简述不同的Node Centrality计算方法

只用Node Degree作为节点重要度，会有什么缺点？

Eigenvector centrality和PageRank有什么异同？

Betweenness Centrality和Closeness Centrality有什么区别？分别揭示了节点是什么特征？

你认为所有海峡中，哪个海峡的Betweenness Centrality最高？

你认为中国所有城市中，哪个城市的Closeness Centrality最高？

湖北到中国任何一个省级行政区，最多跨两个省，说明哪个特征高？

你认为你所在城市的地铁站中，哪个地铁站的Closeness Centrality最高？哪个地铁站的Clutering Coefficient最高？

地铁线路连接关系，应该如何表示？（邻接矩阵、连接列表、邻接列表）

你认为你的人脉圈中，谁的Clutering Coefficient最高？为什么？

什么是Ego-Network（自我中心网络）？

Graphlet和Wavelet（小波分析）有什么异同？

由四个节点组成的图，存在多少种Graphlet？

五个节点构造的所有Graphlet中，存在多少种不同角色的节点？

节点的哪些特征，可以衡量该节点是否为中心枢纽节点？桥接节点？边缘孤立节点？

除了课程中讲的Centrality之外，还有哪些Centrality指标？（PageRank、Katz Centrality、HITS Hubs and Authorities）

# 传统图机器学习方法-连接

## 扩展阅读

NetworkX相关文档

https://networkx.org/documentation/stable/reference/generated/networkx.classes.function.common_neighbors.html

https://networkx.org/documentation/stable/reference/algorithms/generated/networkx.algorithms.link_prediction.jaccard_coefficient.html

https://networkx.org/documentation/stable/reference/algorithms/generated/networkx.algorithms.link_prediction.adamic_adar_index.html

https://stackoverflow.com/questions/62069781/how-to-find-the-similarity-between-pair-of-vertices-using-katz-index-in-python

## 思考题

连接层面，存在哪些数据挖掘任务，有何应用场景？

连接层面可以构造哪些特征？这些特征可以归为哪三类？

简述Link Prediction的基本流程

A和B都知道梅西，C和D都知道同济子豪兄，请问哪对人物更容易产生社交连接。可以用哪个特征解释？

两个节点没有共同好友时，可以用什么特征，将连接编码为D维向量？

简述Katz Index的算法原理

如何计算节点U和节点V之间，长度为K的路径个数

为什么不直接把link两端节点的向量特征concat到一起，作为link的向量特征

# 传统图机器学习方法-全图

## 扩展阅读

https://networkx.org/documentation/stable/reference/algorithms/generated/networkx.algorithms.graph_hashing.weisfeiler_lehman_graph_hash.html

## 思考题

全图层面，存在哪些数据挖掘任务，有何应用场景？

全图层面可以构造哪些特征？

全图层面的Graphlet，和节点层面的Graphlet，有什么区别？

子图匹配，算法复杂度如何计算？

简述Weisfeiler-Lehman Kernel的算法原理

Weisfeiler-Lehman Kernel的词汇表（颜色表）是如何构建的？

Weisfeiler-Lehman Kernel，算法复杂度是多少？

Weisfeiler-Lehman Kernel和图神经网络（GNN）有什么关系？

简述Kernel Methods基本原理

为什么在Graph-level任务中，使用Kernel Methods

除了Graphlet Kernel和Weisfeiler-Lehman Kernel之外，还有哪些Kernel

传统图机器学习和特征工程中，哪些特征用到了邻接矩阵Adjacency Matrix？

如何把无向图节点、连接、全图的特征，推广到有向图？

如何用代码实现Weisfeiler-Lehman Kernel？