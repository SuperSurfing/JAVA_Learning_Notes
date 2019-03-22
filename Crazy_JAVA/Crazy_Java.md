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
  - [继承与组合](#继承与组合)
  - [多态](#多态)
  - [初始化块](#初始化块)
  - [包装类](#包装类)
  - [对象处理](#对象处理)
  - [类成员](#类成员)
  - [final修饰符](#final修饰符)
  - [抽象类与接口](#抽象类与接口)
  - [内部类](#内部类)
  - [lambda表达式](#lambda表达式)
  - [对象与垃圾回收](#对象与垃圾回收)
  - [jar](#jar)
- [CH7-CH10](#ch7-ch10)


### Learning_Plan

参考 [知乎：JAVA 自学入门](https://www.zhihu.com/question/25255189) ：  

![](https://pic1.zhimg.com/80/v2-d941642631a8b3dfcf8f8ed1bbbba3dc_hd.jpg)


参考 [知乎：JAVA 后端自学之路](https://zhuanlan.zhihu.com/p/33716688)

![](https://pic2.zhimg.com/80/v2-67d75dcb8dcd383dd370d83099b69275_hd.jpg)


参考 [Java学习路径及练手项目合集](https://zhuanlan.zhihu.com/p/30782286)

[Crazy JAVA Source Code](https://github.com/DoingLee/crazy-java-src)

[知乎：大数据核心技术](https://www.zhihu.com/question/27696290)



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

**猜测 Java GC 的回收算法**：  
GC 会对比“栈内存”中引用变量指向的地址和“堆内存”中的对象的地址，如果发现“无主对象”，则自动回收该对象的内存。


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

参考 6.11 节“修饰符的适应范围”

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

5.6 节“深入构造器”主要介绍了两个重点：一是“构造器重载”；二是“构造器调用构造器”（参考 5.5 Apple.java 代码，它实际上是使用 this 调用构造器）。

需要注意的是：**JAVA 类只有 constructor 没有 destructor**（析构器），所有的对象都由 GC 自动回收。


#### Methods

> 在结构化编程语言里，函数是一等公民，整个软件是由一个个的函数组成；在面向对象编程语言里，类才是一等公民，整个系统由一个个的类组成。因此在 JAVA 语言里，方法（method）不能独立存在，方法必须属于类或对象。  

为了区分，在 JAVA 中一般称“method”（方法），而不称“函数”（function）。

JAVA Methods 的重点知识：  
- 可变个数形参（简化数组形参）
- 重载（Overload）方法


#### 隐藏和封装

JAVA 的封装增加了 default （包访问权限）访问权限级别，其他的与 C++ 相同。  

参考示例程序 5.4 可以很好的理解 JAVA 的访问控制机制。  

![](https://github.com/SuperSurfing/JAVA_Learning_Notes/blob/master/Crazy_JAVA/Images/AccessRigth.png?raw=true)

#### package

JAVA 引入了 package 的概念，既有C++“名称空间”的作用，又有功能集成（类库）的功效。  

需要仔细阅读 5.4.3 节“package, import and import static”，特别是“包结构与目录结构一一对应”需要注意。此外，包名最好使用全小写，类名用首字母大写。  

> 当虚拟机（JVM）要装载 lee.Hello 类时，它会依次搜索 CLASSPATH 环境变量所指定的系列路径，查找这些路径下是否包含 lee 路径（目录），并在 lee 路径下查找是否包含 Hello.class 文件。  

- package 语句位于整个源文件的第一行（非注释）
- 如果没有显示指定 package 语句，则处于默认包下
- 同一个包下的类可以自由访问
- 父包中的类访问子包中的类，需要用子包路径全名
- 使用 import 可以省略写包名，而使用 import static 则可以连类名都可以省略

JAVA 源文件结构如下：

![](https://github.com/SuperSurfing/JAVA_Learning_Notes/blob/master/Crazy_JAVA/Images/struct.png?raw=true)


#### 继承与组合

与 C++ 不同的是，JAVA 严格限制为“单继承”。  

> Java 使用 extends 作为继承的关键字，它很好地体现子类和父类的关系：子类是父类的扩展。


##### Override vs. Super

1. 子类可以重写（Override）父类的方法，也可以使用 Super 或父类名来调用被覆盖的父类方法
2. Super 还可以用来访问父类被隐藏的成员
3. 子类构造器可以使用 Super 来调用父类构造器


##### is-a vs. has-a

5.8 节介绍了一些比较重要的 OOP 设计思想，is-A or has-A 是一个问题，值得认真揣摩，也可以细细体会示例程序 5.8 。  

Java 的实例成员都是引用类型，所以在设计组合的时候，一般会将被组合对象通过形参传给载体对象的构造器。

父类在设计的时候，需要特别注意那些会被子类 Override 的方法。

#### 多态

> Java 引用变量有两个类型：一个是编译时类型，一个是运行时类型。编译时类型由声明该变量时使用的类型决定，运行时类型由实际赋给该变量的对象决定。如果编译时类型和运行时类型不一致，就可能出现所谓的多态（Polymorphism）。

JAVA 的多态与 C++ 大致相同，通过体验示例程序 5.7 即可掌握。

##### 类型转换

同 C/C++ 一样，Java 的类型转换符也是小括号。不同的是：  
- 数值类型与布尔类型不能互转
- 引用类型只能在继承链上转换
- instanceof 运算符预先判断转换可行性


#### 初始化块

初始化块是 Java 类的第 4 个成员，前面 3 个依次是：成员变量（field）、方法（method）和构造器（constructor）。

> 初始化块只在创建 Java 对象时隐式执行，而且在执行构造器之前执行

初始块的作用是将不同构造器的相同代码段提取出来，减少重复代码。在 javac 编译的时候，它会被自动填充到各个构造器中。  



#### 包装类

包装类（Wrapper）的有两个好处： 
1. 增强 OOP，将 8 个基本类型与 class 统一
2. 包装类提供了很多 convenient methods，比如字符串转换功能：ParseXXX / valueof

示例程序 6.1 “Primitive2String” 演示了字符串与各种基本数据类型的互转。  

此外，可以参考 JAVA API Doc 去了解各个包装类的 features 。


#### 对象处理

6.2 节主要介绍了 Object 的 ToString 方法及其 Override 和 对象比较的方法。  

- ToString
- 恒等号比较 ==
- 值相等比较 equals 方法 override



#### 类成员

Java 的 类成员（包括类变量和类方法等）与 C++ 的静态成员相似，不同的是：**Java 类成员可以通过对象来访问**，JVM 在底层会自动转换为类来访问。

关键：**java 类成员不能访问实例成员**！它们的作用域和初始化时间不同，这种访问容易引起系统混乱。

##### Singleton

6.3 节另一个重要的概念是“如何创建 java 的 Singleton 对象”，参考示例程序 6.3\SingletonTest 。


```
class Singleton
{
	//使用一个变量来缓存曾经创建的实例
	private static Singleton instance;
	
	//将构造器使用private修饰，隐藏该构造器
	private Singleton(){}

	public static Singleton getInstance()
	{
		if (instance == null)
		{
			instance = new Singleton();
		}
		return instance;
	}
}
```


#### final修饰符

Java 的 final 修饰符类似于 C# 的 sealed，兼具部分 C++ 中 const 的功能。它可以修饰 class, local variable, field and methods 。  

由于系统会自动初始化 field ，而不会自动初始化 local variable，因此，final 修饰它们的效果不同。  

field 修饰局部变量和形参时，效果和 C++ 中的 const 差不多。

##### 宏变量

final 可以用于定义“宏变量”，需要理解一些编译原理。

##### final 方法和 final 类

final 方法不可以被重写（override），final 类不可以有子类


##### 缓存实例的不可变类

这一小节演示了一种设计模式——“缓存”，参考示例程序 6.4 - CacheImmutaleTest



#### 抽象类与接口

> 抽象类体现的是一种**模版模式**的设计

6.5 节“抽象类”通过 Shape - calPerimeter 的例子，非常精辟地讲解了“抽象类”在 OOP 中的作用，值得细细体会，特别是该节最后关于“模版模式”的设计规则。  

> 利用抽象类和抽象方法的优势，可以更好地发挥多态的优势，使得程序更加灵活


“抽象类”与 C++ 带虚函数的类相似，但也有很大区别：  
- 关键字不同：abstract vs. virtual
- Java 的抽象类更纯粹：它不能实例化，抽象方法也不能有实现等
- 继承自抽象类的实例类必须实现所有“没有实现的抽象方法”，否则仍被归为抽象类
- final 与 abstract 相冲


##### 模版模式

- 抽象父类可以只定义部分方法，把不能实现的方法留给子类去实现
- 抽象父类的方法可以只是一个**通用算法**，其实现依赖子类的辅助（需调用其他“抽象方法”）。


##### 接口

从实现上来说，接口是一种特殊的抽象类，它没有任何实现的方法。通过 javac 编译后的 interface 仍然是 *.class 文件。但是，从 OOP 来说，接口是一种重要的设计思想，它与抽象类的设计思想完全不同。  

> 抽象类是一种“模版模式”的设计，而接口则体现的是一种“规范”——接口与实现分离。

从设计思想上来说，接口不是一种类，因此，接口不使用 class 关键字，而是用单独的 interface 关键字。  

需要注意的是，接口的定义中会省略很多关键字。可以参考示例程序 6.6 ，认真体会接口的定义。  

重点：**接口支持多继承**，参考示例程序 6.6 - Printer


##### 面向接口编程

这一节通过示例程序 6.6 - Computer.java 和 6.6 - Command.java 分别演示了面向接口编程的**工厂模式**和**命令模式**。它们都降低了模块之间的**耦合性**。  
“简单工程模式”中的 Computer 只与 Output 接口耦合，而不与任何具体的类耦合。此外，OutputFactory 类负责创建具体的 Printer，并在此将 Printer 装载到 Computer 中。  
工程模式的精髓就是有一个专门的“工厂类”负责**将各个组件类组装起来**。  

> 想象一下，在组装车间（Factory）工人将一款 Printer 安装到预留了 output 接口的 Computer 上，这就是工厂模式。如果产品升级了，比如出了一款新的 BetterPrinter ，Computer 生产线完全不需要调整，只需修改组装车间的组装清单，将 BetterPrinter 组装到 Computer 上即可。  
接口是双向的，一方面 Printer 和 BetterPrinter 在生产的时候要遵循 output 接口，另一方面 Computer 也要预留 output 接口。

“命令模式”貌似 vistor （访问者）模式，它的核心是将“处理行为”当作一个参数传给一个“通用方法”。这种模式在函数式编程中很常见，它就是将函数当形参。  
**ProcessArray 就像是一个红娘**，将 array 和 cmd 牵到了一起。

> 想象一下在厨房烹饪的情况，target 是待烹饪的食材，command 是烹饪的方法。比如有一条鱼，它既可以红烧，也可以清蒸，还可以做烤鱼；同样地，一只鸡也可以有炒、炖、烤三种烹饪方式。因此，我们应该将食材和烹饪方法保持互相独立，只有在真正烹饪的时候，才根据顾客点单的情况具体实施某种烹饪方式。    
由此也可以看出，接口是一种模糊的约定，它提供了更大的灵活空间。  



总结一下：无论是“简单工程模式”，还是“命令模式”，它们的核心目的都是降低模块间的耦合。它们的共同实现方法是将各个功能模块尽量拆分为独立的“零件”，然后在通过一个“耦合器”将这些零件耦合在一起，一当有变动，仅需要修改耦合器即可。而这个“耦合器”在“工厂模式”中就是 OutputFactory 类，在“命令模式”中就是 ProcessArray 类。


#### 内部类

内部类又称嵌套类，在 C++ 中也有相似的概念。  

6.7 节介绍了“内部类”的三种用途和相关用法。由于实际项目中并不常见，我们可以先了解其用途即可。



#### lambda表达式

同 C++，Lambda 表达式又称为“箭头表达式” （->），它实际上是一种“匿名函数”。

> Lambda 表达式支持将代码块作为方法参数， Lambda 表达式允许使用更简洁的代码来创建只有一个抽象方法的接口（函数式接口）的示例。  

示例程序 6.8 是在示例程序 6.6 - CommandTest 的基础上，先用内部类进行改进，再用 Lambda 表达式进行更简洁的改进。  


```
public class CommandTest
{
	public static void main(String[] args) 
	{
		ProcessArray pa = new ProcessArray();
		int[] array = {3, -4, 6, 4};
		
		pa.process(array , (int[] target)->{
		        int sum = 0;
		        for (int tmp : target )
		        {
		        	sum += tmp;
		        }
		        System.out.println("数组元素的总和是:" + sum);
		});
	}
}
```

这一节的另一个示例代码演示了几种 Lambda表达式的简写方法。

注意：Lambda表达式只支持与“函数式接口”联用。


#### 枚举类

> 这种实例有限而且固定的类，在 Java 里被称为枚举类。比如：星期、四季等。

```
public enum SeasonEnum
{
	// 在第一行列出4个枚举实例
	SPRING,SUMMER,FALL,WINTER;
}
```

枚举类与普通类不同：  
1. 枚举类使用 enum 修饰，而不是 class
2. 枚举类派生自 java.lang.Enum 而不是 java.lang.Object
3. 枚举类不能派生子类
4. 所有枚举类都有一个values方法，返回该枚举类的所有实例
5. 平常使用枚举实例时，总是通过EnumClass.variable形式来访问

参考 EnumTest 示例程序


```
	public static void main(String[] args)
	{
		//所有枚举类都有一个values方法，返回该枚举类的所有实例
		for (SeasonEnum s : SeasonEnum.values())
		{
			System.out.println(s);
		}
		//平常使用枚举实例时，
		//总是通过EnumClass.variable形式来访问
		new EnumTest().judge(SeasonEnum.SPRING);
	}
```



#### 对象与垃圾回收


![](https://github.com/SuperSurfing/JAVA_Learning_Notes/blob/master/Crazy_JAVA/Images/status.png?raw=true)

这一节主要讲解“对象与垃圾回收”的机制，也不太深，了解即可。


#### JAR

JAR - Java Archive File，它是一种压缩文件，与常见的 zip 文件兼容，通常被称为 JAR 包。

JAR 包一般通过 jar 命令压缩而成，将它添加到 CLASSPATH 后，JVM 能够在内存中自动解压成目录树。  

6.12 节还介绍了 jar 命令的基本用法，它也是基本 Linux 命令之一。需要注意的是，《疯狂JAVA讲义》是在 Windows 环境下演示的，标准 Linux 命令应该在 options 前添加“-”。   





