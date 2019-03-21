### Absract

&emsp;&emsp;�����ǡ����JAVA���塷��ѧϰ�ʼǣ���Ҫ�ܽ� JAVA ��һЩ����֪ʶ�ͱ��ģʽ��  


- [Learning Plan](#learning_plan)
- [CH1-CH4](#ch1-ch4)
  - [��������](#��������)
  - [JAVA��������](#java��������)
  - [UML](#uml)
  - [javadoc](#javadoc)
  - [JAVA�������ͺ������](#java�������ͺ������)
  - [��������ѭ��](#��������ѭ��)
  - [��������](#��������)
  - [Arrays](#arrays)
- [CH5-CH6](#ch5-ch6)
  - [class_and_object](#class_and_object)
  - [constructor_and_this](#constructor_and_this)
  - [Methods](#methods)
  - [���غͷ�װ](#���غͷ�װ)
  - [package](#package)
- [CH7-CH10](#ch7-ch10)


### Learning_Plan

�ο� [֪����JAVA ��ѧ����](https://www.zhihu.com/question/25255189) ��  

![](https://pic1.zhimg.com/80/v2-d941642631a8b3dfcf8f8ed1bbbba3dc_hd.jpg)


�ο� [֪����JAVA �����ѧ֮·](https://zhuanlan.zhihu.com/p/33716688)

![](https://pic2.zhimg.com/80/v2-67d75dcb8dcd383dd370d83099b69275_hd.jpg)


�ο� [Javaѧϰ·����������Ŀ�ϼ�](https://zhuanlan.zhihu.com/p/30782286)

[Crazy JAVA Source Code](https://github.com/DoingLee/crazy-java-src)



### CH1-CH4

#### ��������

CH1 ��Ȼ������ JDK �����غͻ������������ã�����û�н��� IDE �����ã��ڴˣ��ҽ���Щͳһ����һ�¡�  



#### JAVA��������

CH1 ������ JAVA ���ԵĻ�����������л�������Ҫ���յ�֪ʶ�������  
- JVM, JRE, JDK
- [JDK �汾�仯](https://www.jianshu.com/p/31433bcaa1a5)��JAVA SE, JAVA EE, JAVA ME��
- [JDK ������](https://www.oracle.com/technetwork/java/javase/downloads/index.html)����װ�ͻ�����������
- CLASSPATH
- JAVA �ı�������У�javac, java��
- **JAVA ����Ļ�������**��class, source file, pack��
- jshell

ͨ�� procexp.exe ���Թ۲쵽��û����һ�� JAVA ���򣬻ᴴ��һ�� java.exe ���̡���� jave.exe Ӧ�þ��� JVM ��  
���⣬ͨ�� everything Ҳ����������java.exe������javac.exe���͡�javadoc.exe�� �Ƚ��̵� image �ļ���


#### UML

CH2 ���ص��ǽ����� UML �� OOP ��̵�˼�롣  
�ص�������֮��Ĺ�ϵ��[��ͼ](https://www.visual-paradigm.com/guide/uml-unified-modeling-language/uml-aggregation-vs-composition/)����  
- �����������ۺϡ���ϣ�
- ��������̳�ͬһ�����
- ����

�����Ķ� ["UML Association vs Aggregation vs Composition"](https://www.visual-paradigm.com/guide/uml-unified-modeling-language/uml-aggregation-vs-composition/)������һ����������Ӳ�������Щ���

���� OOP ���Բο� [WIKI - Object-oriented programming](https://en.wikipedia.org/wiki/Object-oriented_programming)���� �ǳ��������ܽ��� OOP ��һЩ�ؼ� topics��������  
- Objects and Classes
- Encapsulation ��private, public, static��
- Composition, inheritance, and delegation



#### javadoc

CH3 �ĵ�һ���ص������� javadoc �� [JAVA API Doc](https://docs.oracle.com/javase/8/docs/api/) ���÷���  

**JAVA ��ע�ͷ����� C++ ��ͬ��JAVA �Ĺؼ���Ҳ�� C++ ���ƣ�ȫ��Сд���ʡ�**


#### JAVA�������ͺ������

**JAVA �Ļ����������ͺ���������� C++ ��ͬ��**

![](https://github.com/SuperSurfing/JAVA_Learning_Notes/blob/master/Crazy_JAVA/Images/type.png?raw=true)

��Ҫע����� JAVA �������ݽ��ƣ�  
- ������ 0b / 0B ��ͷ
- �˽��� 0 �㿪ͷ
- ʮ���ƣ����㿪ͷ
- ʮ�����ƣ�0x / 0X ��ͷ


#### ��������ѭ��

**JAVA �ġ�������䡢��֧����ѭ����䡱������صĹؼ����� C++ �����ƶȴ� 99% !**


#### ��������

JAVA ������Ҳ��һ�֡����͡����Ƽ�ʹ����������д���������������������͵����塣 

```
type[] arrayName 
```

> JAVA ������һ���������͵ı��������ʹ��������һ������ʱ��������ʾ������һ�����ñ�����ָ�룩��������ñ�����δָ���κ��ڴ棬��˶�������ʱ����ָ������ĳ��ȡ�  

�����ԣ�JAVA ����� C++ ��������ȫ��ͬ�ĸ�������ӽ� C++ ָ�롣  
JAVA ������ص㣺  
- ��ʼ��ʱҪ�õ� new �ؼ���
- foreach ѭ����ͬ C++ 11��
- JAVA ����洢�ڶ��ڴ棨heap����
- Ҫ�����������������/ָ�룩�����ݵ�����
- ��ά����ı���

���� JAVA ���飬������ϸ���ʾ������ 4.5 �� 4.6 ��


#### Arrays

Arrays �� JAVA 8 �ṩ��һ�������࣬���ṩ�����������������磺�����ݲ��ҡ��������򡱵ȡ�     
ͨ������ API �ĵ��͵���ʾ������ 4.6 ���ɴ����˽⣬�ر������е� Gobang.java ��ʾ�˶�ά������÷���  




### CH5-CH6

CH5 �� CH6 ��Ҫ���� JAVA ��������̵Ļ��ơ�  

#### class_and_object

JAVA ���� C++ ��Ĳ�֮ͬ�����£�  
- JAVA ʹ�� extends �ؼ�����ʾ��ʾ�̳й�ϵ
- JAVA �����������η���pulic, final, and abstract��Ҳ����ȱʡ
- public ��������ļ�ͬ��
- ���� final ��Ա������field�����η�
- ���� final �� abstract ��Ա�������η�
- û�� virtual ���η�


**JAVA ��������� new �ؼ��ʴ��������£�**   

```
//����һ��Person���͵ı���
Person p;

//ͨ��new�ؼ��ֵ���Person��Ĺ�����������һ��Personʵ����
//����Personʵ������p������
p = new Person();

//��p������ֵ��ֵ��p2����
Person p2 = p;
```

�����ԣ�**JAVA �������Ա���洢�ڡ����ڴ桱��**�����ǡ��ֲ��������洢�ڡ�ջ�ڴ桱�С�


#### constructor_and_this

JAVA ��� constructor �� C++ ���ƣ�Ҳ�� default constructor ��  

JAVA û��ָ�룬��ˣ�JAVA �е� this �ǡ�this ���á���


#### Methods

> �ڽṹ����������������һ�ȹ��������������һ�����ĺ�����ɣ����������������������һ�ȹ�������ϵͳ��һ����������ɡ������ JAVA �����������method�����ܶ������ڣ�������������������  

Ϊ�����֣��� JAVA ��һ��ơ�method�����������������ơ���������function����

JAVA Methods ���ص�֪ʶ��  
- �ɱ�����βΣ��������βΣ�
- ���أ�Overload������


#### ���غͷ�װ

JAVA �ķ�װ������ default ��������Ȩ�ޣ�����Ȩ�޼����������� C++ ��ͬ��  

�ο�ʾ������ 5.4 ���Ժܺõ���� JAVA �ķ��ʿ��ƻ��ơ�  

#### package

JAVA ������ package �ĸ������C++�����ƿռ䡱�����ã����й��ܼ��ɣ���⣩�Ĺ�Ч��  

��Ҫ��ϸ�Ķ� 5.4.3 �ڡ�package, import and import static�����ر��ǡ����ṹ��Ŀ¼�ṹһһ��Ӧ����Ҫע�⡣���⣬�������ʹ��ȫСд������������ĸ��д��  

> ���������JVM��Ҫװ�� lee.Hello ��ʱ�������������� CLASSPATH ����������ָ����ϵ��·����������Щ·�����Ƿ���� lee ·����Ŀ¼�������� lee ·���²����Ƿ���� Hello.class �ļ���  

- package ���λ������Դ�ļ��ĵ�һ�У���ע�ͣ�
- ���û����ʾָ�� package ��䣬����Ĭ�ϰ���
- ͬһ�����µ���������ɷ���
- �����е�������Ӱ��е��࣬��Ҫ���Ӱ�·��ȫ��
- ʹ�� import ����ʡ��д��������ʹ�� import static �����������������ʡ��





