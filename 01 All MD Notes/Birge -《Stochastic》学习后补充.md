第一遍看 《Introduction to stochastic programming》，里面涉及到很多没有学习过的知识所以没有学懂，在这里进行一些补充

## 基本理论方面

[心态与做事习惯决定人生高度的博客_CSDN博客-数学优化,心情随笔,java领域博主](https://chenzhen.blog.csdn.net/?type=bbs)

这位老师的博客有很多能参考的地方。也是做管科的。

### 测度论中的概率空间

[测度论中的概率空间_心态与做事习惯决定人生高度的博客-CSDN博客_概率空间](https://chenzhen.blog.csdn.net/article/details/125884260)

> 概率空间（probability space）是测度论的基本概念，测度论将传统积分进行了进一步推广。传统的积分在一个区间上进行，而测度论将积分推广到可以在一个集合中进行。

确实，之前一直不理解为什么积分可以在集合中进行，原来是测度论的主要工作

## 方法论

### 重要性采样（Importance Sampling）

[(99+ 封私信 / 80 条消息) 重要性采样 - 搜索结果 - 知乎 (zhihu.com)](https://www.zhihu.com/search?type=content&q=重要性采样)

蒙特卡罗积分法解决的问题是积分曲线难以解析，无法直接求积分。

重要性采样则在此基础上增加准确度，减少方差（不是解决能不能采样的问题，而是解决采样法得到的方差过大的问题）。方法为根据重要性重新定义一个权重。

### 抽样平均近似方法 Sample average approximation(SAA)

[抽样平均近似方法 Sample Average Approximation （SAA）_心态与做事习惯决定人生高度的博客-CSDN博客_抽样平均近似法](https://blog.csdn.net/robert_chen1988/article/details/90319257)

[随机优化中的样本均值近似方法_王有福的博客-CSDN博客_样本平均近似](https://blog.csdn.net/wdl1992/article/details/108410404)

> 看下来给我的感觉和蒙特卡罗差不多啊。是不是说SAA就是将蒙特卡罗思想运用到随机规划的结果？