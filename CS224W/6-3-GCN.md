# 图卷积神经网络GCN

> 同济子豪兄 2023-3-8
>

## 视频

中文精讲视频：https://www.bilibili.com/video/BV1Hs4y157Ls

Youtube视频：https://www.youtube.com/watch?v=MH4yvtgAR-4&list=PLoROMvodv4rPLKxIpqhjhPgdQy7imNkDn&index=19

## 本讲介绍

斯坦福大学CS224W图机器学习公开课-同济子豪兄中文精讲

课程大纲、中文笔记课件、论文笔记、代码、思考题、扩展阅读、答疑群：https://github.com/TommyZihao/zihao_course/tree/main/CS224W

本讲介绍了最简单的一类图神经网络：图卷积神经网络（GCN）

包括：消息传递计算图、聚合函数、数学形式、Normalized Adjacency 矩阵推导、计算图改进、损失函数、训练流程、实验结果。

图神经网络相比传统方法的优点：归纳泛化能力、参数量少、利用属性特征和节点标签等。

图神经网络和CNN、Transformer等其它神经网络的异同。

GCN论文：Semi-Supervised Classification with Graph Convolutional Networks, ICLR 2017

关键词：
Machine Learning, Deep Learning, Neural Networks, Graph Neural Networks, GNN, Graph Convolutional Neural Networks, GCN, Knowledge Graph

## 扩展阅读

论文主页：https://arxiv.org/abs/1609.02907

官方代码：https://github.com/tkipf/gcn

作者本人写的博客：https://tkipf.github.io/graph-convolutional-networks

博客：https://www.inference.vc/how-powerful-are-graph-convolutions-review-of-kipf-welling-2016-2

博客：https://ireneli.eu/2019/01/08/understanding-graph-convolutional-networks

李沐老师推荐的GNN博客1：https://distill.pub/2021/gnn-intro

李沐老师推荐的GNN博客2：https://distill.pub/2021/understanding-gnns

Normalized Adjacency Matrix推导过程：https://math.stackexchange.com/questions/3035968/interpretation-of-symmetric-normalised-graph-adjacency-matrix

《图神经网络 基础、前沿与应用》人民邮电出版社 异步图书社区，部分章节电子版

https://graph-neural-networks.github.io

五折购书（正版全新）：公众号 人工智能小技巧 回复 城堡书



在线编辑LaTex公式网站：https://www.latexlive.com

和D矩阵相关的数学公式LaTex脚本：

```latex
{\color{Blue} h_{v}^{(k+1)} }  = {\color{Green} \sigma(} {\color{Red} W_{k}} \sum_{u\in N(v)} \frac{{\color{Blue} h_{u}^{k}} }{|N(v)|}{\color{Green} )} 



D = 
\begin{bmatrix} 
  & d(1) & 0 & 0 & \cdots & 0  &\\
  
  & 0 & d(2) & 0 & \cdots & 0   \\

  & 0 & 0 & d(3)  & \cdots & 0 \\
  & \vdots & \vdots & \vdots & \ddots & \vdots\\

  & 0 & 0 & 0 & \cdots & d(n)
\end{bmatrix}

D^{-1} = 
\begin{bmatrix} 
  & \frac{1}{d(1)} & 0 & 0 & \cdots & 0  &\\
  
  & 0 & \frac{1}{d(2)} & 0 & \cdots & 0   \\

  & 0 & 0 & \frac{1}{d(3)}  & \cdots & 0 \\
  & \vdots & \vdots & \vdots & \ddots & \vdots\\

  & 0 & 0 & 0 & \cdots & \frac{1}{d(n)}
\end{bmatrix}

D^{\frac{1}{2}} = 
\begin{bmatrix} 
  & \sqrt{d(1)} & 0 & 0 & \cdots & 0  &\\
  
  & 0 & \sqrt{d(2)} & 0 & \cdots & 0   \\

  & 0 & 0 & \sqrt{d(3)}  & \cdots & 0 \\
  & \vdots & \vdots & \vdots & \ddots & \vdots\\

  & 0 & 0 & 0 & \cdots & \sqrt{d(n)}
\end{bmatrix}

D^{-\frac{1}{2}} = 
\begin{bmatrix} 
  & \frac{1}{\sqrt{d(1)}} & 0 & 0 & \cdots & 0  &\\
  
  & 0 & \frac{1}{\sqrt{d(2)}} & 0 & \cdots & 0   \\

  & 0 & 0 & \frac{1}{\sqrt{d(3)}}  & \cdots & 0 \\
  & \vdots & \vdots & \vdots & \ddots & \vdots\\

  & 0 & 0 & 0 & \cdots & \frac{1}{\sqrt{d(n)}}
\end{bmatrix}
```

## 思考题

GCN的计算图是如何构建的？

图神经网络的层数是如何计算的？

神经网络层数越多，图神经网络也越深吗？

理论上图神经网络可以任意深，实际上可行吗？

GCN的聚合函数是什么？

简述GCN的数学形式

简述Normalized Adjacency Matrix的推导过程

为什么要引入Self Embedding？

“图卷积”和“图像卷积”有什么异同？

如何通过监督学习的方式训练图神经网络？

如何通过无监督（自监督）学习的方式训练图神经网络？

为什么图神经网络具有归纳式学习能力？

图神经网络的参数量如何计算？

图神经网络具有哪些优点？

GCN能否使用节点的属性？为什么？

GCN能否使用连接的属性？为什么？

GCN还具有哪些缺点？（表达能力、聚合函数）

GCN可以解决哪些图机器学习问题？

如何理解“卷积神经网络是图神经网络的特例”？

如何理解“Transformer是图神经网络的特例”？

## 特别感谢

赵冰辰（爱丁堡大学）、李沐（亚马逊）、张军斌（图科学实验室）