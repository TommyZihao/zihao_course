# 改变世界的谷歌PageRank算法

## 视频

Pagerank算法讲解：https://www.bilibili.com/video/BV1uP411K7yN

PageRank代码实战-西游记人物重要度：https://www.bilibili.com/video/BV1Wg411H7Ep

斯坦福CS224W图机器学习、图神经网络公开课【同济子豪兄中文精讲】：https://github.com/TommyZihao/zihao_course/tree/main/CS224W

## 算法概述

Page L, Brin S, Motwani R, et al. The PageRank citation ranking: Bringing order to the web[R]. Stanford InfoLab, 1999.

PageRank是1997年谷歌第一代搜索引擎的底层算法。大幅提高了搜索结果的相关率和质量，成为互联网第一个爆款应用，造就了传奇的谷歌公司。

PageRank是搜索引擎、信息检索、图机器学习、知识图谱、线性代数必读经典算法。

PageRank把互联网表示为由网页节点和引用链接构成的有向图，通过链接结构，计算网页节点重要度。来自重要网页节点的引用链接，权重更高。

通过线性方程组、矩阵乘法、特征值和特征向量、随机游走、马尔科夫链，五种角度，理解并求解PageRank值。讲解PageRank的收敛性分析及针对特殊节点的改进方法，最后扩展PageRank在推荐系统中计算节点相似度排序的升级变种。

在代码实战中，使用Networkx计算四大名著人物有向图的节点重要度。

![image-20221207100140686](改变世界的谷歌PageRank算法.assets/image-20221207100140686.png)

## 参考PPT

黑底白色PPT：斯坦福CS224W图机器学习

https://web.stanford.edu/class/cs224w

纯黑底PPT：PageRank: A Trillion Dollar Algorithm（作者：Reducible）

https://www.youtube.com/watch?v=JGQe4kiPnrU

绿底PPT：Google‘s PageRank Algorithm（作者：Global Software Support）

https://www.youtube.com/playlist?list=PLH7W8KdUX6P2n4XwDiKsEU6sBhQj5cAqa

曼彻斯特大学：https://personalpages.manchester.ac.uk/staff/yanghong.huang/teaching/MATH36032/pagerank.pdf

斯坦福CS345 Data Mining：https://wenku.baidu.com/view/5be822bfbb4cf7ec4bfed052.html?_wkts_=1669773903123&bdQuery=web+in+1839

## 参考视频

https://www.youtube.com/watch?v=meonLcN7LD4

https://www.youtube.com/watch?v=P8Kt6Abq_rM&list=PLH7W8KdUX6P2n4XwDiKsEU6sBhQj5cAqa&index=4

PageRank与马尔科夫链：https://www.youtube.com/watch?v=JGQe4kiPnrU

## 其它参考资料

《数学之美》（作者：吴军）， 人民邮电出版社

得到APP：张潇雨·商业经典案例课-谷歌

得到APP：吴军·谷歌方法论

PageRank原始论文1：http://infolab.stanford.edu/~backrub/google.html

PageRank原始论文2：http://ilpubs.stanford.edu:8090/422

## 思考题

PageRank值可以被恶意刷高吗？

PageRank为什么被称为“民主自治”算法？

简述理解和计算PageRank的几个角度：线性方程组、矩阵左乘、特征向量、随机游走、马尔科夫链

PageRank假设某节点的所有出链接权重相同，这是否足够合理？如何改进？

Spider Trap和Dead End节点，会对求解PageRank值产生什么影响？如何改进？改进方法足够科学吗？

Random Teleport概率β的值，会对求解PageRank值产生什么影响？

PageRank、Personlized PageRank、RandomWalk with Restart，这三种算法有什么区别？

求解PageRank时，为什么求解线性方程组和矩阵特征值的算法复杂度是O(n^3)？

求解PageRank时，为什么最终选择了简单粗暴的Power Iteration（幂迭代）？

Damping Factor设置为一个常数，是否足够科学？（看完抖音后更可能看开微博，而不是公开课网站）