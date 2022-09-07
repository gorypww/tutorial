Java是由C++开发的

# C++快速入门

[TOC]

# P1

## OO-Objective Oriented

c语言快、精炼、小巧。相比之下，c++代码量比较大，会为了解决问题绕一大圈。c++有个绝对优势，针对不同对象进行实例化，就是所谓的OO思想

### 什么是OO思想

任何事物都可以看做一个对象。将复杂模型看作千万个对象组成（分而治之）。彼此之间互相联系、组合。每个对象有两个要素：属性和行为。

## 比较

### 面向过程和面向对象的区别

（1）**面向过程**：面向过程编程就是分析出解决问题的步骤，然后把这些步骤一步一步的实现，使用的时候一个一个的依次调用就可以了。
（2）**面向对象**：面向对象编程就是把问题分解成各个对象，建立对象的目的不是为了完成一个步骤，而是为了描述某个事物在整个解决问题的步骤中的行为。

### 面向过程和面向对象的优缺点

**·** **面向过程语言**

优点：性能比面向对象高，因为类调用时需要实例化，开销比较大，比较消耗资源;比如[单片机](https://www.zhihu.com/search?q=单片机&search_source=Entity&hybrid_search_source=Entity&hybrid_search_extra={"sourceType"%3A"article"%2C"sourceId"%3A"320280579"})、[嵌入式开发](https://www.zhihu.com/search?q=嵌入式开发&search_source=Entity&hybrid_search_source=Entity&hybrid_search_extra={"sourceType"%3A"article"%2C"sourceId"%3A"320280579"})、 Linux/Unix等一般采用面向过程开发，性能是最重要的因素。
缺点：没有面向对象易维护、易复用、易扩展

**·** **面向对象语言**：

优点：易维护、易复用、易扩展，由于面向对象有封装、继承、多态性的特性，可以设计出低耦合的系统，使系统 更加灵活、更加易于维护
缺点：性能比面向过程低

## 特点

### 封装

封装意味着把对象的属性0方法结合成一个独立的奈统单位，并尽可能隐藏对象的内部细节

### 抽象



### 继承



### 多态

多态是指在基类中定义的属性和行为被子类继后，可以且有不同的数据类型或者表现行为等特性。（共性中寻找特性）

# P2

通过用C++编写。相同功能的C程序来实现

## 传递指针，而不是数组

## 程序分析

### cout-console out

### 输出流

### using namespace std 名字空间

 C++标谁库所使用的所有标识符（即类函数、对象等的名称)都是在同一个特殊的名字空间(std)中来定义的。防止大型项目协同开发时一些变量已经被命名。

### << 流操作符

重载。不同的语境有不同的应用。

# P3

## 头文件库

### cin属于istream属于

### cin>>i

输入操作符，一次从cin中提取一个整数

### 阻塞

不进行键盘的输入

### >> 右移操作符

用于从输入流对象提取信息

###  c++可以再任意位置声明变量

### cin和cout的语法

#### cin.ignore() cin.getline()

c&c++的字符串以0结尾，string[20]仅能输入19个字符

#### cin.get() cin.peek()

#### cin.gcount() cin.read

#### cout.precision() cout.width()

# P4

## 文件I/O

fileCopy

## c++文件操作

#include<fstream>

# P5输入输出小结



# P6函数的重载

重载不是面相对对象的基本特征，只是简化编程的一种方案。

通过不同传入参数的数值类型进行重载，相同传入函数叫做覆盖。

# P7-11 复杂的数据类型

**复杂=简单+简单**

## 数组

声明为某一特定的类型

type name[size]

### 宏定义（define）和常量（const unsigned short）的区别

未解决

## 指针

创建指针时空格放在哪里都可以

int * p1; int *p1

### 取址操作符：&

##  利用指针改变值

### 解引用

*p1 = 123，i.e.，通过指针改变指针的值

（“ * ”的两个作用：1.创建指针；2.解引用）

### 无类型指针

## 指针和数组

![image-20220728145558670](C:\Users\GoryPww\AppData\Roaming\Typora\typora-user-images\image-20220728145558670.png)

**指针指向数组的第一个元素，指针自加即可访问下一个元素**

## 结构

自定义数据类型（定义数据结构！），面向对象的核心。

```c++
struct name {

​	type varName1;
    type varName2;

}
```

# P12传值、传址和传引用

被传递到函数的只是变量的值，永远不会是变量本身。

## 传地址

函数声明的时候用*表示指针

函数内部用*表示解引用

main中函数传入参数用&取址

## 传引用

和传地址的目的一样，语法更容易使用。

**声明的时候直接&取址**

# P13 联合、枚举和类型别名

## 联合

联合与结构有很多相以之处，可以容纳多种不同类型的值，但是它每次只能存储这些值中的某一个。改变时会覆盖。

```c++
union mima{

​	...

}
```

## 枚举

不用引号，因为编译为数值

作用：1.对变量的取值加以限制；2.作为switch语句的case标号。

## 类型别名

typedef int* intPointer; (数据结构)

# P14 对象（OOP）

类是一个模型，对象本身是创建的实例

对象内部有变量和函数，结构只有变量

```c++
class Car
{
public:
    static const float FULL_GAS = 85 //除了静态常量，其他都不可以赋值
	std::string color;
    std::string engine;
    float gas_tank;
    usigned int Wheel;
    
    void fill_tank(float liter);// 方法的声明
};

void Car::fill_tank(float liter)
{
    ...
}
// "::"作用域解析符，表示这个方法是来自于Car类中的

int main
{
    Car mycar;
    mycar.fill_tank;
    return 0;
}
```

# P16 构造器和析构器

## 构造器

作为一种方法，在类里面声明，外面详细说明，进行类的初始化。

如果没有自定义构造器，编译器会定义空构造器。

```c++
class Car
{
	...
	Car(void)
	...
};

Car::Car(void)
{
	color;
    engine;
    gas_tank;
    int Wheel;	
}
```

## 构造对象数组

```c++
Car mycar[10];
mycar[x].running
```

## 析构器

销毁对象、清理对象。

```c++
~ClassName();
```

#  P17 this指针

## this指针

指向当前类生成的对象

```c++
class Human{
	char fishc;
	Human(char fishc);
}
Human:Human(char fishc){
	this -> fishc = fishc;
    //左边为当前对象的属性，右边为构造器传入的fishc参数。
}
```

## 类的继承

```c++
class SubClass : public SuperClass {...}

class Pig : public Animal {...}
```

```c++
class Animal
{
public:
    std::string mouth;
    
    void eat();
    void slepp();
    void drool();
}

class Pig : Animal
{
public:
    void climb();
};

class Turtle : public Animal
{
public: 
    void swim(); 
};

void Animal::eat(){}
void Animal::slepp(){}
void Animal::drool(){}
...
void Pig::climb(){}
...
    
int main()
{
    Pig pig;
    Turtle turtle;
    
    pig.eat();
    pig.climb();
    xxx
}

```

# P18继承中的构造器和析构器

```c++
Animal::animal( std::string theName ){
	name = theName;
}

Pig::Pig( std::string theName ):Animal( theName ){}
```

# P19访问控制

保护类的方法和属性的手段。对谁可以访问某个方法和属性加上限制，若无权访问则报错。

## public

```c++
pig.name = "xxx" // 可以直接修改

class Pig:(public/protected/private) Animal {...} //public不做任何修改；protected，将原public改为protected
```

## bug

BUG无法避免的原因正是因为我门无法模拟各种情况的的输入和修改带来的影响.

# P20覆盖和重载

继承后的重载会出问题。

# P21友元关系

# P22-23静态属性和静态方法

## 目的

非必要的时候不要使用全局变量

在创建和删除对象的时候才允许访问的计数器——静态属性和静态函数

有关数据在该类所有对象之间都可以共享

## static静态变量

## 作用

### 隐藏

### 

## 静态方法

# P24虚方法

# P25抽象方法

## =0

## 多态

一个方法，多种实现



























































































































































































































































































