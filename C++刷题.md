# C++刷题

## 链表

### [2181. 合并零之间的节点](https://leetcode.cn/problems/merge-nodes-in-between-zeros/)

#### [C++ for 循环 | 菜鸟教程 (runoob.com)](https://www.runoob.com/cplusplus/cpp-for-loop.html)

#### 结构

加入伪头结点，方便输出；加入尾结点，方便末尾插入。

第二种方法：原地修改。直接在原链表上进行修改，少用一个指针，占用内存更少。

#### “?”运算符

### [2130. 链表最大孪生和](https://leetcode.cn/problems/maximum-twin-sum-of-a-linked-list/)

快慢指针（找到中间节点）+反转链表，其中反转链表如何写在**206**

### [1290. 二进制链表转整数](https://leetcode.cn/problems/convert-binary-number-in-a-linked-list-to-integer/)

为什么用左移操作符速度快这么多？

### [面试题 04.03. 特定深度节点链表](https://leetcode.cn/problems/list-of-depth-lcci/)

queue::front()返回对第一个元素的引用。

涉及到queue的pop(), front(), empty(), push()

vector的push_back()等众多知识

### [剑指 Offer II 024. 反转链表](https://leetcode.cn/problems/UHnkqh/)

递归方法还不太懂

[C++ &&、||、！逻辑运算符用法详解 (biancheng.net)](http://c.biancheng.net/view/1360.html)

### [剑指 Offer 06. 从尾到头打印链表](https://leetcode.cn/problems/cong-wei-dao-tou-da-yin-lian-biao-lcof/)

vector和操作方法，应该是数组有相关题目。

### [382. 链表随机节点](https://leetcode.cn/problems/linked-list-random-node/)

####  vector.emplace_back()

vector.emplace_back()和push_back()差不多，前者效率更高。

#### 随机数

rand() % i == 0) { // 1/i 的概率选中（替换为答案）

rand() % arr.size()

### [116. 填充每个节点的下一个右侧](https://leetcode.cn/problems/populating-next-right-pointers-in-each-node/)

和树有关，简单看一看，没做。

### [剑指 Offer 35. 复杂链表的复制](https://leetcode.cn/problems/fu-za-lian-biao-de-fu-zhi-lcof/)

哈希（Hash），也叫散列，是第七章搜索的内容。

第二种方法本质也是哈希，学了之后再说吧。

### [剑指 Offer II 023. 两个链表的第一个](https://leetcode.cn/problems/3u1WK4/)

没想到...

### [1206. 设计跳表](https://leetcode.cn/problems/design-skiplist/)

hard题直接不看

### [面试题 02.01. 移除重复节点](https://leetcode.cn/problems/remove-duplicate-node-lcci/)

$O(n^2)$的方法想都没想，$O(n)$的方法要用到哈希表。