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

## 栈

### [1614. 括号的最大嵌套深度](https://leetcode.cn/problems/maximum-nesting-depth-of-the-parentheses/)

使用

```cpp
for (char c : s)
1
```

时会复制一个s字符串再进行遍历操作，而使用

```cpp
for (char& c : s)
1
```

时直接引用原字符串进行遍历操作。由于复制一个字符串花费了大量的时间，所以第二种解法要快于第一种解法。

### [1381. 设计一个支持增量操作的栈](https://leetcode.cn/problems/design-a-stack-with-increment-operation/)

[C++ vector的用法（整理）_一个幽默且帅气的程序员的博客-CSDN博客_c++ vector](https://blog.csdn.net/wkq0825/article/details/82255984)

```cpp
if (top != stk.size() - 1) //正确
if (top < stk.size() - 1) //出错
```

因为stk.size()为无符号整型，要改成(int)stk.size()。

[(19条消息) 有(无)符号整型变量_try hard️的博客-CSDN博客_无符号整型](https://blog.csdn.net/m0_60869584/article/details/123140702)

#### 迭代器

[vector::iterator it_淼淼1111的博客-CSDN博客_vector::iterator](https://blog.csdn.net/u010112268/article/details/81111086)

[C++迭代器_Zhc_AuC的博客-CSDN博客_c++ 迭代器](https://blog.csdn.net/weixin_41368411/article/details/124222020)

#### stack的相关操作 包括push() & emplace() 的区别

[C++ 栈（stack）使用简述_地球被支点撬走啦的博客-CSDN博客_c++栈](https://blog.csdn.net/Flag_ing/article/details/123554966)

### [1047. 删除字符串中的所有相邻重复项](https://leetcode.cn/problems/remove-all-adjacent-duplicates-in-string/)

[C++ 字符串（string）常用操作总结_地球被支点撬走啦的博客-CSDN博客_c++ 字符串操作](https://blog.csdn.net/Flag_ing/article/details/123361432)

不能用负数下标访问容器；需要先`int n = ans.size();`，在用[n-1]访问后几位。

#### switch 和 if else

　   A:　从某种程度上，Switch/case比if/else的效率要高，除非if/else在第一次逻辑判断就为true；

　　B:　Switch/case需要建立一张跳转表，因此需要一定的空间的，更像是以空间换效率。

　　C:　if/else能进行逻辑判断，而Switch不行,因此在需要进行逻辑判断时使用if/else语句；

### [496. 下一个更大元素 I](https://leetcode.cn/problems/next-greater-element-i/)

简单是因为暴力求解的简单。哈希表没有学，他可以通过值进行映射，实现O(1)的查找功能。

## 队列

### [950. 按递增顺序显示卡牌](https://leetcode.cn/problems/reveal-cards-in-increasing-order/)

[C++——deque_qw&jy的博客-CSDN博客_c++ deque](https://blog.csdn.net/qq_43448856/article/details/123009040)
