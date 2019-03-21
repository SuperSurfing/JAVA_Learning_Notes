### Absract

&emsp;&emsp;本文是《疯狂JAVA讲义》的学习笔记，主要总结 JAVA 的一些基本知识和编程模式。  


- [Learning Plan](#learning_plan)
- [CH1-CH4](#ch1-ch4)
  - [开发环境](#开发环境)
  - [JAVA基本概念](#java基本概念)
  - [UML](#uml)
  - [javadoc](#javadoc)
  - [JAVA基本类型和运算符](#java基本类型和运算符)
  - [条件语句和循环](#条件语句和循环)
  - [数组类型](#数组类型)
  - [Arrays](#arrays)
- [CH5-CH6](#ch5-ch6)
  - [class_and_object](#class_and_object)
  - [constructor_and_this](#constructor_and_this)
  - [Methods](#methods)
  - [隐藏和封装](#隐藏和封装)
  - [package](#package)
- [CH7-CH10](#ch7-ch10)


### Learning_Plan

参考 [知乎：JAVA 自学入门](https://www.zhihu.com/question/25255189) ：  

![](https://pic1.zhimg.com/80/v2-d941642631a8b3dfcf8f8ed1bbbba3dc_hd.jpg)


参考 [知乎：JAVA 后端自学之路](https://zhuanlan.zhihu.com/p/33716688)

![](https://pic2.zhimg.com/80/v2-67d75dcb8dcd383dd370d83099b69275_hd.jpg)


参考 [Java学习路径及练手项目合集](https://zhuanlan.zhihu.com/p/30782286)

[Crazy JAVA Source Code](https://github.com/DoingLee/crazy-java-src)



### CH1-CH4

#### 开发环境

CH1 虽然介绍了 JDK 的下载和环境变量的配置，但是没有介绍 IDE 的配置，在此，我将这些统一介绍一下。  



#### JAVA基本概念

CH1 介绍了 JAVA 语言的基本概念和运行环境，需要掌握的知识点包括：  
- JVM, JRE, JDK
- [JDK 版本变化](https://www.jianshu.com/p/31433bcaa1a5)（JAVA SE, JAVA EE, JAVA ME）
- [JDK 的下载](https://www.oracle.com/technetwork/java/javase/downloads/index.html)，安装和环境变量配置
- CLASSPATH
- JAVA 的编译和运行（javac, java）
- **JAVA 程序的基本规则**（class, source file, pack）
- jshell

通过 procexp.exe 可以观察到，没运行一个 JAVA 程序，会创建一个 java.exe 进程。这个 jave.exe 应该就是 JVM 。  
此外，通过 everything 也可搜索到“java.exe”、“javac.exe”和“javadoc.exe” 等进程的 image 文件。


#### UML

CH2 的重点是介绍了 UML 和 OOP 编程的思想。  
重点掌握类之间的关系（[类图](https://www.visual-paradigm.com/guide/uml-unified-modeling-language/uml-aggregation-vs-composition/)）：  
- 关联（包括聚合、组合）
- 泛化（与继承同一个概念）
- 依赖

建议阅读 ["UML Association vs Aggregation vs Composition"](https://www.visual-paradigm.com/guide/uml-unified-modeling-language/uml-aggregation-vs-composition/)，它用一个形象的例子阐述了这些概念。

关于 OOP 可以参考 [WIKI - Object-oriented programming](https://en.wikipedia.org/wiki/Object-oriented_programming)，它 非常精练地总结了 OOP 的一些关键 topics，包括：  
- Objects and Classes
- Encapsulation （private, public, static）
- Composition, inheritance, and delegation



#### javadoc

CH3 的第一个重点是掌握 javadoc 和 [JAVA API Doc](https://docs.oracle.com/javase/8/docs/api/) 的用法。  

**JAVA 的注释方法与 C++ 相同，JAVA 的关键字也与 C++ 相似，全是小写单词。**


#### JAVA基本类型和运算符

**JAVA 的基本数据类型和运算符都与 C++ 相同。**

![](https://github.com/SuperSurfing/JAVA_Learning_Notes/blob/master/Crazy_JAVA/Images/type.png?raw=true)

需要注意的是 JAVA 四种数据进制：  
- 二进制 0b / 0B 开头
- 八进制 0 零开头
- 十进制，非零开头
- 十六进制，0x / 0X 开头


#### 条件语句和循环

**JAVA 的“条件语句、分支语句和循环语句”及其相关的关键词与 C++ 的相似度达 99% !**


#### 数组类型

JAVA 的数组也是一种“类型”，推荐使用下面这种写法，它更能体现数组类型的语义。 

```
type[] arrayName 
```

> JAVA 数组是一种引用类型的变量，因此使用它定义一个变量时，仅仅表示定义了一个引用变量（指针），这个引用变量还未指向任何内存，因此定义数组时不能指定数组的长度。  

很明显，JAVA 数组和 C++ 数组是完全不同的概念，它更接近 C++ 指针。  
JAVA 数组的特点：  
- 初始化时要用到 new 关键字
- foreach 循环（同 C++ 11）
- JAVA 数组存储在堆内存（heap）中
- 要区分数组变量（引用/指针）与数据的数组
- 二维数组的本质

关于 JAVA 数组，可以仔细体会示例程序 4.5 和 4.6 。


#### Arrays

Arrays 是 JAVA 8 提供的一个工具类，它提供了许多便利函数，比如：“二份查找”、“排序”等。     
通过查阅 API 文档和调试示例程序 4.6 即可大致了解，特别是其中的 Gobang.java 演示了二维数组的用法。  




### CH5-CH6

CH5 和 CH6 主要介绍 JAVA 面向对象编程的机制。  

#### class_and_object

JAVA 类与 C++ 类的不同之处如下：  
- JAVA 使用 extends 关键字显示表示继承关系
- JAVA 类有三个修饰符：pulic, final, and abstract，也可以缺省
- public 类必须与文件同名
- 增加 final 成员变量（field）修饰符
- 增加 final 和 abstract 成员函数修饰符
- 没有 virtual 修饰符


**JAVA 对象必须以 new 关键词创建，如下：**   

```
//定义一个Person类型的变量
Person p;

//通过new关键字调用Person类的构造器，返回一个Person实例，
//将该Person实例赋给p变量。
p = new Person();

//将p变量的值赋值给p2变量
Person p2 = p;
```

很明显，**JAVA 对象及其成员都存储在“堆内存”中**，但是“局部变量”存储在“栈内存”中。


#### constructor_and_this

JAVA 类的 constructor 与 C++ 类似，也有 default constructor 。  

JAVA 没有指针，因此，JAVA 中的 this 是“this 引用”。


#### Methods

> 在结构化编程语言里，函数是一等公民，整个软件是由一个个的函数组成；在面向对象编程语言里，类才是一等公民，整个系统由一个个的类组成。因此在 JAVA 语言里，方法（method）不能独立存在，方法必须属于类或对象。  

为了区分，在 JAVA 中一般称“method”（方法），而不称“函数”（function）。

JAVA Methods 的重点知识：  
- 可变个数形参（简化数组形参）
- 重载（Overload）方法


#### 隐藏和封装

JAVA 的封装增加了 default （包访问权限）访问权限级别，其他的与 C++ 相同。  

参考示例程序 5.4 可以很好的理解 JAVA 的访问控制机制。  

#### package

JAVA 引入了 package 的概念，既有C++“名称空间”的作用，又有功能集成（类库）的功效。  

需要仔细阅读 5.4.3 节“package, import and import static”，特别是“包结构与目录结构一一对应”需要注意。此外，包名最好使用全小写，类名用首字母大写。  

> 当虚拟机（JVM）要装载 lee.Hello 类时，它会依次搜索 CLASSPATH 环境变量所指定的系列路径，查找这些路径下是否包含 lee 路径（目录），并在 lee 路径下查找是否包含 Hello.class 文件。  

- package 语句位于整个源文件的第一行（非注释）
- 如果没有显示指定 package 语句，则处于默认包下
- 同一个包下的类可以自由访问
- 父包中的类访问子包中的类，需要用子包路径全名
- 使用 import 可以省略写包名，而使用 import static 则可以连类名都可以省略





