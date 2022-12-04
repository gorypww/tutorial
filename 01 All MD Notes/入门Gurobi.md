# Gurobi入门课程

> [网络讲座视频汇总-学习资料-Gurobi 中国](http://www.gurobi.cn/picexhview.asp?id=90)

[TOC]

## 课程一 基本操作

<img src="C:\Users\GoryPww\AppData\Roaming\Typora\typora-user-images\image-20221203145246277.png" alt="image-20221203145246277" style="zoom:33%;" />

### TupleList

#### Select方法

<img src="C:\Users\GoryPww\AppData\Roaming\Typora\typora-user-images\image-20221203150051186.png" alt="image-20221203150051186" style="zoom:33%;" />

也就是说，这个Tuplelist是通过特殊的Select方法帮助我们在构造约束条件的时候快速筛选出符合条件的变量。如果用不到Select，那么就没有必要用Tuplelist。

> [Gurobi自学笔记—常用数据结构tuplelist和tupledict - 知乎 (zhihu.com)](https://zhuanlan.zhihu.com/p/108721362)
>
> 给了一个例子，还没有看懂

#### Gurobi变量一般都是tupledict类型。

所以对模型中变量进行操作时可以直接用select方法。

### Prop函数

<img src="C:\Users\GoryPww\AppData\Roaming\Typora\typora-user-images\image-20221203153006822.png" alt="image-20221203153006822" style="zoom:33%;" />

### 建模过程

<img src="C:\Users\GoryPww\AppData\Roaming\Typora\typora-user-images\image-20221203153218786.png" alt="image-20221203153218786" style="zoom:33%;" />

#### 定义数据

<img src="C:\Users\GoryPww\AppData\Roaming\Typora\typora-user-images\image-20221203154539564.png" alt="image-20221203154539564" style="zoom:67%;" />

<img src="C:\Users\GoryPww\AppData\Roaming\Typora\typora-user-images\image-20221203154703016.png" alt="image-20221203154703016" style="zoom:67%;" />

<img src="C:\Users\GoryPww\AppData\Roaming\Typora\typora-user-images\image-20221203154559359.png" alt="image-20221203154559359" style="zoom:67%;" />

通过一个multidict同时定义多个数据。包括一个tuplelist和多个tupledict

![image-20221203154957209](C:\Users\GoryPww\AppData\Roaming\Typora\typora-user-images\image-20221203154957209.png)

<img src="C:\Users\GoryPww\AppData\Roaming\Typora\typora-user-images\image-20221203155005551.png" alt="image-20221203155005551" style="zoom:67%;" />

根据food下标定义变量，并且名称为name+[index]

## 课程二

### 模型参数设置

[参数说明文档](D:\下载\Gurobi\学习资料\refman.pdf)

gurobi在求解的时候，整数变量（0-1变量）也以浮点数据在进行处理，因此在最终结果中可能会带小数。误差在1e-5内，都算作正常误差。
如果想得到不带小数的结果，需要设置 IntegralityFocus （仅限 9.1 或以后版本）参数，即：可以设置为：

```
m.Params.IntegralityFocus=1
```

#### 自动调参

### 广义约束

#### max/min

<img src="https://pic2.zhimg.com/v2-43d3c70a3618dd0b125fa48552e92c39_r.jpg" alt="img" style="zoom: 33%;" />

#### abs

#### ans/or

此时无论变量被定义为何种形式，都会被解析为0-1变量

#### 指示函数

#### 范围函数

#### SOS约束

SOS_TYPE1 表示一组有序变量中最多有一个变量取值不为0；

SOS_TYPE2 表示一组有序变量中最多有两个变量取值不为0,且非零变量相邻。变量是否相邻由权重决定。

### 特殊目标函数

#### 多目标

#### 分段函数

#### 线性函数逼近非线性

### Solution Pool 

Gurobi在搜寻最优解的过程中,会找到一些次优解(sub-optimal solutions),有时候用户也希望知道次优解的具体

情况。因此Gurobi会将计算过程中发现的所有解记录在Solution Pool里供用户查询。

## 课程三 高级操作

### Callback

允许用户在Gurobi**求解过程中**获取信息、终止优化、加入额外约束条件(割平面)、加入自己开发的算法等。

#### 取

#### "_变量名"

<img src="C:\Users\GoryPww\AppData\Roaming\Typora\typora-user-images\image-20221203224822470.png" alt="image-20221203224822470" style="zoom:67%;" />

> 不知道是什么意思

#### 用法

割平面（cut），Lazy cut，开发启发式算法

### 广义约束线性化

## 课程四 列生成和 Benders 分解

### 列生成

#### Reduce Cost就是检验数

#### 例子（Cutting Stock Problem）

##### 初始切割模式

##### 加入新的切割模式，对应检验数小于0

在[学习文档](C:\Users\GoryPww\Desktop\tutorial2\02 Py or Ipynb\001 Gurobi 模板\入门Gurobi.ipynb)中删除了原本的注释，添加自己理解的注释。

### Benders分解

> [优化算法 | Benders Decomposition: 一份让你满意的【入门-编程实战-深入理解】的学习笔记 - 知乎 (zhihu.com)](https://zhuanlan.zhihu.com/p/513518225)

假定复杂的变量是已经确定了的

## 课程五

给了两个例子，题目描述的不够完全、PPT有比较多错误的地方、老师也念PPT理解起来没那么容易。不过里面python处理表格数据并结合Gurobi的做法有空可以去参考一下。