# C++刷题

[TOC]

## 每日一题

### [790. 多米诺和托米诺平铺](https://leetcode.cn/problems/domino-and-tromino-tiling/) （动态规划 / 思维+找规律）

#### 动态规划

``考虑这么一种平铺的方式：在第 *i* 列前面的正方形都被瓷砖覆盖，在第 *i* 列后面的正方形都没有被瓷砖覆盖（*i*从 11 开始计数）。``这种定义方式比较不容易想到。想到之后可以O(n, n)内解决。

#### 思维

怎么样找到规律，需要找到一中不可分割的结构，保证这种结构在之前的递归答案中不会出现。

### [剑指 Offer II 113. 课程顺序](https://leetcode.cn/problems/QA2IGt/)

看了题解之后才会做

新的知识点--在遍历搜索中，如果图可能成环：vis数组设置为三种不同的搜索状态——未搜索、在搜索和已搜索。

### [808. 分汤](https://leetcode.cn/problems/soup-servings/)

[error: call to implicitly-deleted default constructor of ‘unordered_map＜pair＜int, int＞, int＞‘ m；_Zhihao杨的博客-CSDN博客](https://blog.csdn.net/weixin_42989041/article/details/113183015)

[C++STL—pair＜int,int＞与unordered_map的结合使用_shadow_lr的博客-CSDN博客](https://blog.csdn.net/lr_shadow/article/details/115864228)







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

### [1425. 带限制的子序列和](https://leetcode.cn/problems/constrained-subsequence-sum/)

如何想到如下方法的预定义动态规划呢。

> 我们用 *f[i]* 表示在数组的前 *i* 个数中进行选择，并且恰好选择了第 *i* 个数，可以得到的最大和。

## 串

### [1455. 检查单词是否为句中其他单](https://leetcode.cn/problems/check-if-a-word-occurs-as-a-prefix-of-any-word-in-a-sentence/)

bool isPrefix(const string &sentence, int start, int end, const string &searchWord) {

其中的const [(19条消息) c++ const 用法_coolwriter的博客-CSDN博客_c++ const](https://blog.csdn.net/coolwriter/article/details/100135873)

[【C++】为什么要尽可能使用const?_人工智能博士的博客-CSDN博客_为什么要用const](https://blog.csdn.net/qq_15698613/article/details/85245248)

### [1408. 数组中的字符串匹配](https://leetcode.cn/problems/string-matching-in-an-array/)

words[j].find(words[i]) != string::npos

```cpp
int i,j = 0; //相当于声明了变量i,j 但只给j赋值0
```

### [剑指 Offer II 085. 生成匹配的括号](https://leetcode.cn/problems/IDBivT/)

思路有点像 从枚举到隐枚举。

用到了回溯算法。

### [1769. 移动所有球到每个盒子所需](https://leetcode.cn/problems/minimum-number-of-operations-to-move-all-balls-to-each-box/)

```cpp
class Solution {
public:
    vector<int> minOperations(string boxes) {
        vector<int> res(boxes.size(),0);
        for (int i = 0; i < boxes.size(); i++){
            for (int j = 0; j < boxes.size(); j++){
                int dis = i-j>0?i-j:j-i;
                res[j] += (int)(boxes[i]-48)*dis;
            }
        }
        return res;
    }
};
```

$n^{2}$方法

### 2194.Excel 表中某个范围内的单元格

通过定义字符串方法将char转化为string：

```cpp
string cell(1, row);
```

### [1773. 统计匹配检索规则的物品数量](https://leetcode.cn/problems/count-items-matching-a-rule/)

```cpp
s = ruleKey=="name"? 2: ruleKey=="color";
```

一下子搞了两个三目运算，就很帅！

### [2255. 统计是给定字符串前缀的字符](https://leetcode.cn/problems/count-prefixes-of-a-given-string/) & [2185. 统计包含给定前缀的字符串](https://leetcode.cn/problems/counting-words-with-a-given-prefix/)

[C++之string的compare用法 - 程嘿嘿 - 博客园 (cnblogs.com)](https://www.cnblogs.com/cff2121/p/9989806.html)

```cpp
compare(int start,int end, compared_object)
```

### [1528. 重新排列字符串](https://leetcode.cn/problems/shuffle-string/)

[C++ 中的Swap函数写法汇总_C 语言_脚本之家 (jb51.net)](https://www.jb51.net/article/181427.htm)

``swap()``

## 树

### [剑指 Offer II 055. 二叉搜索树迭代器](https://leetcode.cn/problems/kTOapQ/)

官方题解中第二种做法，通过栈实时进行迭代中序遍历。

```cpp
    int next() {  // 初始时 cur = root
        while (cur != nullptr) {
            stk.push(cur);
            cur = cur->left;
        }
        cur = stk.top();
        stk.pop();
        int ret = cur->val;
        cur = cur->right;
        return ret;
    }
```



```cpp
        stack<int> s;
        TreeNode* res = new TreeNode(nums[0]);
        nums.erase(0,1);
        
        for (auto num:nums) {
            if (num>res->val) {
                res = new TreeNode(num, res, nullptr);
            } else {
                TreeNode* cur = res;
                while (cur && num < cur->val){
                    cur = cur->right;
                }
                res->left = new TreeNode(num, nullptr, cur);
            }

            
        }
    }
```

## 图

### [1319. 连通网络的操作次数](https://leetcode.cn/problems/number-of-operations-to-make-network-connected/)

[并查集（详细解释+完整C语言代码）_～在下小吴的博客-CSDN博客_并查集代码](https://blog.csdn.net/weixin_54186646/article/details/124477838)

```cpp
// 并查集模板
class Djset {
private:
    vector<int> parent;  // 记录节点的根
    vector<int> rank;  // 记录根节点的深度（用于优化）
    int count;         // 记录连通分量的个数
    int rest;          // 记录多余的连接数
public:
    Djset(int n): parent(vector<int>(n)), rank(vector<int>(n)), count(n), rest(0) {
        for (int i = 0; i < n; i++) {
            parent[i] = i;
        }
    }
    
    int find(int x) {
        // 压缩方式：直接指向根节点
        if (x != parent[x]) {
            parent[x] = find(parent[x]);
        }
        return parent[x];
    }
    
    void merge(int x, int y) {
        int rootx = find(x);
        int rooty = find(y);
        if (rootx != rooty) {
            // 按秩合并
            if (rank[rootx] < rank[rooty]) {
                swap(rootx, rooty);
            }
            parent[rooty] = rootx;
            if (rank[rootx] == rank[rooty]) rank[rootx] += 1;
            count--;
        } else {
            rest++;
        }
    }
    int getCount() {
        return count;
    }
    int getRest() {
        return rest;
    }
};

class Solution {
public:
    int makeConnected(int n, vector<vector<int>>& connections) {
        Djset ds(n);
        for (auto& e :connections) {
            ds.merge(e[0], e[1]);
        }
        if (ds.getRest() < ds.getCount() - 1) return -1;
        return ds.getCount() - 1;
    }
};

```

### [1368. 使网格图至少有一条有效路](https://leetcode.cn/problems/minimum-cost-to-make-at-least-one-valid-path-in-a-grid/)

### [743. 网络延迟时间](https://leetcode.cn/problems/network-delay-time/)

#### Dijkstra 算法中的小根堆

[C++优先队列priority_queue详解_是一只派大鑫的博客-CSDN博客_c++ priority_queue](https://blog.csdn.net/weixin_44572229/article/details/121925067)



## 查找 (二分查找)

### [222. 完全二叉树的节点个数](https://leetcode.cn/problems/count-complete-tree-nodes/)

迭代做法的时间复杂度和空间复杂度都为O(n)，可以通过二分查找的思想进行优化，涉及到以下知识点：

#### 位运算

[c++之位运算（详解，初学者绝对能看懂）_？！？？的博客-CSDN博客_c++位运算](https://blog.csdn.net/m0_64183293/article/details/122519405)

### [349. 两个数组的交集](https://leetcode.cn/problems/intersection-of-two-arrays/)

#### unordered_map & set

[C++中的set、unordered_set、map、unordered_map详解以及如何选择_小居老师的博客-CSDN博客_unordered_map unordered_set](https://blog.csdn.net/weixin_52244492/article/details/124628733)

### [731. 我的日程安排表 II](https://leetcode.cn/problems/my-calendar-ii/)

#### map

#### 线段树

```cpp
class MyCalendarTwo {
public:
    MyCalendarTwo() {

    }

    void update(int start, int end, int val, int l, int r, int idx) {
        if (r < start || end < l) {   //
            return;
        } 
        if (start <= l && r <= end) { // [start, end) 区间内的节点进行如下操作(更新最大值和最小值)
            tree[idx].first += val; // val为1或-1，first为区间的最大值，second为区间的最小值
            tree[idx].second += val;
        } else { // 遍历或创造左右节点
            int mid = (l + r) >> 1;
            update(start, end, val, l, mid, 2 * idx);
            update(start, end, val, mid + 1, r, 2 * idx + 1);
            tree[idx].first = tree[idx].second + max(tree[2 * idx].first, tree[2 * idx + 1].first);
        }
    }

    bool book(int start, int end) {            
        update(start, end - 1, 1, 0, 1e9, 1);
        if (tree[1].first > 2) {
            update(start, end - 1, -1, 0, 1e9, 1);
            return false;
        }
        return true;	
    }
private:
    unordered_map<int, pair<int, int>> tree;
};

```

### [1011. 在 D 天内送达包裹的能力](https://leetcode.cn/problems/capacity-to-ship-packages-within-d-days/)

#### 为什么会想到用二分搜索

遇到这种让你找答案的，你不能通过表达式去求得结果，然后问题又具有单调性（重要，二分搜索必须具有单调性），这种问题一般是二分搜索去猜答案。

#### 函数里面再写函数（没有找到规范语法）

[c++ 函数内置函数的写法_yihuo524的博客-CSDN博客](https://blog.csdn.net/yihuo524/article/details/124650839)

### [300. 最长递增子序列](https://leetcode.cn/problems/longest-increasing-subsequence/)

两种解法，我觉得都是动态规划的思想

#### 定义d*[*i*]为考虑前 i 个元素，以第 *i* 个数字结尾的最长上升子序列的长度

#### 维护一个数组d*[*i*] ，表示长度为 i*i* 的最长上升子序列的末尾元素的最小值

### [1170. 比较字符串最小字母出现频次](https://leetcode.cn/problems/compare-strings-by-frequency-of-the-smallest-character/)

#### [（C++）upper_bound()和upper_bound()函数用法_Hunter Dreamer的博客-CSDN博客_upper_bound函数](https://blog.csdn.net/qq_41448334/article/details/123088225)



## 查找（哈希表）

### 

#### C++ unordered_map和unordered_set的区别

[C++ set与map、unordered_map、unordered_set与哈希表_普通网友的博客-CSDN博客_c++ set哈希表](https://blog.csdn.net/m0_67390963/article/details/124503599)

### [1636. 按照频率将数组升序排序](https://leetcode.cn/problems/sort-array-by-increasing-frequency/)

#### sort函数自定义

[C++ Sort函数详解_zhangbw~的博客-CSDN博客_c++ sort](https://blog.csdn.net/VariatioZbw/article/details/125155432)

#### lamba表达式代替

[C++中的Lambda表达式_Monkey Ji的博客-CSDN博客_c++ lambda 表达式](https://blog.csdn.net/Appleeatingboy/article/details/121676559)

其中 **capture list** = [&] 表示以引用方式捕获块外的所有变量。



## 排序

### [1561. 你可以获得的最大硬币数目](https://leetcode.cn/problems/maximum-number-of-coins-you-can-get/)

```cpp
class Solution {
public:
    int maxCoins(vector<int>& piles) {
        sort(piles.begin(), piles.end());
        int ans = 0;
        for (int i = piles.size()-2; i>= (int)piles.size()/3; i = i-2) {
            ans += piles[i];
        }
        return ans;
    }
};
```

为什么循环里判断条件如果没有 `(int)`就会出错？

### [451. 根据字符出现频率排序](https://leetcode.cn/problems/sort-characters-by-frequency/)

#### 桶排序

[基数排序、桶排序和计数排序的区别_LTELTY的博客-CSDN博客_桶排序和基数排序的区别](https://blog.csdn.net/qq_25026989/article/details/89367954)

### [剑指 Offer II 076. 数组中的第 k 大的](https://leetcode.cn/problems/xx4gT2/)

#### 快速排序

### [389. 找不同](https://leetcode.cn/problems/find-the-difference/)

#### 异或计算

异或运算的特性：

1.异或自己得0，任何数异或0得自己本身；
2.具有交换律、结合律，例如 1^2^3^4^2^3^1 = (1^1)^(2^2)^(3^3)^4 = 0^0^0^4 = 0^4 = 4;
总结：异或运算擅长找不同。

### [169. 多数元素](https://leetcode.cn/problems/majority-element/)

#### Boyer-Moore 投票算法

[多数投票算法——Boyer–Moore majority vote algorithm - lkltcl - 博客园 (cnblogs.com)](https://www.cnblogs.com/lkltcl/p/15378722.html)
