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
  - [�̳������](#�̳������)
  - [��̬](#��̬)
  - [��ʼ����](#��ʼ����)
  - [��װ��](#��װ��)
  - [������](#������)
  - [���Ա](#���Ա)
  - [final���η�](#final���η�)
  - [��������ӿ�](#��������ӿ�)
  - [�ڲ���](#�ڲ���)
  - [lambda���ʽ](#lambda���ʽ)
  - [ö����](#ö����)
  - [��������������](#��������������)
  - [jar](#jar)
- [CH7-CH10](#ch7-ch10)
  - [System_and_Runtime](#system_and_runtime)
  - [������](#������)
  - [���ʻ����ʽ��](#���ʻ����ʽ��)


### Learning_Plan

�ο� [֪����JAVA ��ѧ����](https://www.zhihu.com/question/25255189) ��  

![](https://pic1.zhimg.com/80/v2-d941642631a8b3dfcf8f8ed1bbbba3dc_hd.jpg)


�ο� [֪����JAVA �����ѧ֮·](https://zhuanlan.zhihu.com/p/33716688)

![](https://pic2.zhimg.com/80/v2-67d75dcb8dcd383dd370d83099b69275_hd.jpg)


�ο� [Javaѧϰ·����������Ŀ�ϼ�](https://zhuanlan.zhihu.com/p/30782286)

[Crazy JAVA Source Code](https://github.com/DoingLee/crazy-java-src)

[֪���������ݺ��ļ���](https://www.zhihu.com/question/27696290)


������ϵĲο����ϣ��ر��ǡ�JAVA���ѧϰ֮·������һ�׶��Ұ�װ���²�����ѧϰ�����JAVA���塷��  

- ������� CH1-CH4����Ϥ JAVA �����俪���Ļ�������
  - ��⡰һ�н��ࡱ�� JAVA - OOP ˼��
  - ͨ����JAVA���顱����⡰�������͡���**ջ�ڴ�**ָ��**���ڴ�**�ı���
- ����ѧϰ CH5-CH6������ JAVA �������ı��ģʽ��ʵ�ַ���
- GUI ���ֵ� CH11 - AWT ��ƽ̨�Բֱ��������CH12 - Swing ��ʱ����
- 




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

[Java��JDK�汾�Ĺ�ϵ](https://blog.51cto.com/cnn237111/1641194)

ͨ�� procexp.exe ���Թ۲쵽��û����һ�� JAVA ���򣬻ᴴ��һ�� java.exe ���̡���� jave.exe Ӧ�þ��� JVM ��  
���⣬ͨ�� everything Ҳ����������java.exe������javac.exe���͡�javadoc.exe�� �Ƚ��̵� image �ļ���

**�²� Java GC �Ļ����㷨**��  
GC ��Աȡ�ջ�ڴ桱�����ñ���ָ��ĵ�ַ�͡����ڴ桱�еĶ���ĵ�ַ��������֡��������󡱣����Զ����ոö�����ڴ档


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

�ο� 6.11 �ڡ����η�����Ӧ��Χ��

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

5.6 �ڡ����빹��������Ҫ�����������ص㣺һ�ǡ����������ء������ǡ����������ù����������ο� 5.5 Apple.java ���룬��ʵ������ʹ�� this ���ù���������

��Ҫע����ǣ�**JAVA ��ֻ�� constructor û�� destructor**���������������еĶ����� GC �Զ����ա�


#### Methods

> �ڽṹ����������������һ�ȹ��������������һ�����ĺ�����ɣ����������������������һ�ȹ�������ϵͳ��һ����������ɡ������ JAVA �����������method�����ܶ������ڣ�������������������  

Ϊ�����֣��� JAVA ��һ��ơ�method�����������������ơ���������function����

JAVA Methods ���ص�֪ʶ��  
- �ɱ�����βΣ��������βΣ�
- ���أ�Overload������


#### ���غͷ�װ

JAVA �ķ�װ������ default ��������Ȩ�ޣ�����Ȩ�޼����������� C++ ��ͬ��  

�ο�ʾ������ 5.4 ���Ժܺõ���� JAVA �ķ��ʿ��ƻ��ơ�  

![](https://github.com/SuperSurfing/JAVA_Learning_Notes/blob/master/Crazy_JAVA/Images/AccessRigth.png?raw=true)

#### package

JAVA ������ package �ĸ������C++�����ƿռ䡱�����ã����й��ܼ��ɣ���⣩�Ĺ�Ч��  

��Ҫ��ϸ�Ķ� 5.4.3 �ڡ�package, import and import static�����ر��ǡ����ṹ��Ŀ¼�ṹһһ��Ӧ����Ҫע�⡣���⣬�������ʹ��ȫСд������������ĸ��д��  

> ���������JVM��Ҫװ�� lee.Hello ��ʱ�������������� CLASSPATH ����������ָ����ϵ��·����������Щ·�����Ƿ���� lee ·����Ŀ¼�������� lee ·���²����Ƿ���� Hello.class �ļ���  

- package ���λ������Դ�ļ��ĵ�һ�У���ע�ͣ�
- ���û����ʾָ�� package ��䣬����Ĭ�ϰ���
- ͬһ�����µ���������ɷ���
- �����е�������Ӱ��е��࣬��Ҫ���Ӱ�·��ȫ��
- ʹ�� import ����ʡ��д��������ʹ�� import static �����������������ʡ��

JAVA Դ�ļ��ṹ���£�

![](https://github.com/SuperSurfing/JAVA_Learning_Notes/blob/master/Crazy_JAVA/Images/struct.png?raw=true)


#### �̳������

�� C++ ��ͬ���ǣ�JAVA �ϸ�����Ϊ�����̳С���  

> Java ʹ�� extends ��Ϊ�̳еĹؼ��֣����ܺõ���������͸���Ĺ�ϵ�������Ǹ������չ��


##### Override vs. Super

1. ���������д��Override������ķ�����Ҳ����ʹ�� Super �����������ñ����ǵĸ��෽��
2. Super �������������ʸ��౻���صĳ�Ա
3. ���๹��������ʹ�� Super �����ø��๹����


##### is-a vs. has-a

5.8 �ڽ�����һЩ�Ƚ���Ҫ�� OOP ���˼�룬is-A or has-A ��һ�����⣬ֵ�����洧Ħ��Ҳ����ϸϸ���ʾ������ 5.8 ��  

Java ��ʵ����Ա�����������ͣ������������ϵ�ʱ��һ��Ὣ����϶���ͨ���βδ����������Ĺ�������

��������Ƶ�ʱ����Ҫ�ر�ע����Щ�ᱻ���� Override �ķ�����

#### ��̬

> Java ���ñ������������ͣ�һ���Ǳ���ʱ���ͣ�һ��������ʱ���͡�����ʱ�����������ñ���ʱʹ�õ����;���������ʱ������ʵ�ʸ����ñ����Ķ���������������ʱ���ͺ�����ʱ���Ͳ�һ�£��Ϳ��ܳ�����ν�Ķ�̬��Polymorphism����

JAVA �Ķ�̬�� C++ ������ͬ��ͨ������ʾ������ 5.7 �������ա�

##### ����ת��

ͬ C/C++ һ����Java ������ת����Ҳ��С���š���ͬ���ǣ�  
- ��ֵ�����벼�����Ͳ��ܻ�ת
- ��������ֻ���ڼ̳�����ת��
- instanceof �����Ԥ���ж�ת��������


#### ��ʼ����

��ʼ������ Java ��ĵ� 4 ����Ա��ǰ�� 3 �������ǣ���Ա������field����������method���͹�������constructor����

> ��ʼ����ֻ�ڴ��� Java ����ʱ��ʽִ�У�������ִ�й�����֮ǰִ��

��ʼ��������ǽ���ͬ����������ͬ�������ȡ�����������ظ����롣�� javac �����ʱ�����ᱻ�Զ���䵽�����������С�  



#### ��װ��

��װ�ࣨWrapper�����������ô��� 
1. ��ǿ OOP���� 8 ������������ class ͳһ
2. ��װ���ṩ�˺ܶ� convenient methods�������ַ���ת�����ܣ�ParseXXX / valueof

ʾ������ 6.1 ��Primitive2String�� ��ʾ���ַ�������ֻ����������͵Ļ�ת��  

���⣬���Բο� JAVA API Doc ȥ�˽������װ��� features ��


#### ������

6.2 ����Ҫ������ Object �� ToString �������� Override �� ����Ƚϵķ�����  

- ToString
- ��ȺűȽ� ==
- ֵ��ȱȽ� equals ���� override



#### ���Ա

Java �� ���Ա��������������෽���ȣ��� C++ �ľ�̬��Ա���ƣ���ͬ���ǣ�**Java ���Ա����ͨ������������**��JVM �ڵײ���Զ�ת��Ϊ�������ʡ�

�ؼ���**java ���Ա���ܷ���ʵ����Ա**�����ǵ�������ͳ�ʼ��ʱ�䲻ͬ�����ַ�����������ϵͳ���ҡ�

##### Singleton

6.3 ����һ����Ҫ�ĸ����ǡ���δ��� java �� Singleton ���󡱣��ο�ʾ������ 6.3\SingletonTest ��


```
class Singleton
{
	//ʹ��һ����������������������ʵ��
	private static Singleton instance;
	
	//��������ʹ��private���Σ����ظù�����
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


#### final���η�

Java �� final ���η������� C# �� sealed����߲��� C++ �� const �Ĺ��ܡ����������� class, local variable, field and methods ��  

����ϵͳ���Զ���ʼ�� field ���������Զ���ʼ�� local variable����ˣ�final �������ǵ�Ч����ͬ��  

field ���ξֲ��������β�ʱ��Ч���� C++ �е� const ��ࡣ

##### �����

final �������ڶ��塰�����������Ҫ���һЩ����ԭ��

##### final ������ final ��

final ���������Ա���д��override����final �಻����������


##### ����ʵ���Ĳ��ɱ���

��һС����ʾ��һ�����ģʽ���������桱���ο�ʾ������ 6.4 - CacheImmutaleTest



#### ��������ӿ�

> ���������ֵ���һ��**ģ��ģʽ**�����

6.5 �ڡ������ࡱͨ�� Shape - calPerimeter �����ӣ��ǳ����ٵؽ����ˡ������ࡱ�� OOP �е����ã�ֵ��ϸϸ��ᣬ�ر��Ǹý������ڡ�ģ��ģʽ������ƹ���  

> ���ó�����ͳ��󷽷������ƣ����Ը��õط��Ӷ�̬�����ƣ�ʹ�ó���������


�������ࡱ�� C++ ���麯���������ƣ���Ҳ�кܴ�����  
- �ؼ��ֲ�ͬ��abstract vs. virtual
- Java �ĳ���������⣺������ʵ���������󷽷�Ҳ������ʵ�ֵ�
- �̳��Գ������ʵ�������ʵ�����С�û��ʵ�ֵĳ��󷽷����������Ա���Ϊ������
- final �� abstract ���


##### ģ��ģʽ

- ���������ֻ���岿�ַ������Ѳ���ʵ�ֵķ�����������ȥʵ��
- ������ķ�������ֻ��һ��**ͨ���㷨**����ʵ����������ĸ�������������������󷽷�������


##### �ӿ�

��ʵ������˵���ӿ���һ������ĳ����࣬��û���κ�ʵ�ֵķ�����ͨ�� javac ������ interface ��Ȼ�� *.class �ļ������ǣ��� OOP ��˵���ӿ���һ����Ҫ�����˼�룬�������������˼����ȫ��ͬ��  

> ��������һ�֡�ģ��ģʽ������ƣ����ӿ������ֵ���һ�֡��淶�������ӿ���ʵ�ַ��롣

�����˼������˵���ӿڲ���һ���࣬��ˣ��ӿڲ�ʹ�� class �ؼ��֣������õ����� interface �ؼ��֡�  

��Ҫע����ǣ��ӿڵĶ����л�ʡ�Ժܶ�ؼ��֡����Բο�ʾ������ 6.6 ���������ӿڵĶ��塣  

�ص㣺**�ӿ�֧�ֶ�̳�**���ο�ʾ������ 6.6 - Printer


##### ����ӿڱ��

��һ��ͨ��ʾ������ 6.6 - Computer.java �� 6.6 - Command.java �ֱ���ʾ������ӿڱ�̵�**����ģʽ**��**����ģʽ**�����Ƕ�������ģ��֮���**�����**��  
���򵥹���ģʽ���е� Computer ֻ�� Output �ӿ���ϣ��������κξ��������ϡ����⣬OutputFactory �ฺ�𴴽������ Printer�����ڴ˽� Printer װ�ص� Computer �С�  
����ģʽ�ľ��������һ��ר�ŵġ������ࡱ����**�������������װ����**��  

> ����һ�£�����װ���䣨Factory�����˽�һ�� Printer ��װ��Ԥ���� output �ӿڵ� Computer �ϣ�����ǹ���ģʽ�������Ʒ�����ˣ��������һ���µ� BetterPrinter ��Computer ��������ȫ����Ҫ������ֻ���޸���װ�������װ�嵥���� BetterPrinter ��װ�� Computer �ϼ��ɡ�  
�ӿ���˫��ģ�һ���� Printer �� BetterPrinter ��������ʱ��Ҫ��ѭ output �ӿڣ���һ���� Computer ҲҪԤ�� output �ӿڡ�

������ģʽ��ò�� vistor �������ߣ�ģʽ�����ĺ����ǽ���������Ϊ������һ����������һ����ͨ�÷�����������ģʽ�ں���ʽ����кܳ����������ǽ��������βΡ�  
**ProcessArray ������һ������**���� array �� cmd ǣ����һ��

> ����һ���ڳ�����⿵������target �Ǵ���⿵�ʳ�ģ�command ����⿵ķ�����������һ���㣬���ȿ��Ժ��գ�Ҳ���������������������㣻ͬ���أ�һֻ��Ҳ�����г���������������⿷�ʽ����ˣ�����Ӧ�ý�ʳ�ĺ���⿷������ֻ��������ֻ����������⿵�ʱ�򣬲Ÿ��ݹ˿͵㵥���������ʵʩĳ����⿷�ʽ��    
�ɴ�Ҳ���Կ������ӿ���һ��ģ����Լ�������ṩ�˸�������ռ䡣  



�ܽ�һ�£������ǡ��򵥹���ģʽ�������ǡ�����ģʽ�������ǵĺ���Ŀ�Ķ��ǽ���ģ������ϡ����ǵĹ�ͬʵ�ַ����ǽ���������ģ�龡�����Ϊ�����ġ��������Ȼ����ͨ��һ���������������Щ��������һ��һ���б䶯������Ҫ�޸���������ɡ����������������ڡ�����ģʽ���о��� OutputFactory �࣬�ڡ�����ģʽ���о��� ProcessArray �ࡣ


#### �ڲ���

�ڲ����ֳ�Ƕ���࣬�� C++ ��Ҳ�����Ƶĸ��  

6.7 �ڽ����ˡ��ڲ��ࡱ��������;������÷�������ʵ����Ŀ�в������������ǿ������˽�����;���ɡ�



#### lambda���ʽ

ͬ C++��Lambda ���ʽ�ֳ�Ϊ����ͷ���ʽ�� ��->������ʵ������һ�֡�������������

> Lambda ���ʽ֧�ֽ��������Ϊ���������� Lambda ���ʽ����ʹ�ø����Ĵ���������ֻ��һ�����󷽷��Ľӿڣ�����ʽ�ӿڣ���ʾ����  

ʾ������ 6.8 ����ʾ������ 6.6 - CommandTest �Ļ����ϣ������ڲ�����иĽ������� Lambda ���ʽ���и����ĸĽ���  


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
		        System.out.println("����Ԫ�ص��ܺ���:" + sum);
		});
	}
}
```

��һ�ڵ���һ��ʾ��������ʾ�˼��� Lambda���ʽ�ļ�д������

ע�⣺Lambda���ʽֻ֧���롰����ʽ�ӿڡ����á�


#### ö����

> ����ʵ�����޶��ҹ̶����࣬�� Java �ﱻ��Ϊö���ࡣ���磺���ڡ��ļ��ȡ�

```
public enum Chessman {
	BLACK("��"), WHITE("��");
	private final String chessman;

	private Chessman(String chessman) {
		this.chessman = chessman;
	}

	public String getChessman() {
		return this.chessman;
	}
}
```

ö��������ͨ�಻ͬ��  
1. ö����ʹ�� enum ���Σ������� class
2. ö���������� java.lang.Enum ������ java.lang.Object
3. ����ö���඼��һ��values���������ظ�ö���������ʵ��
4. ö�����ʵ��ֻ����ö��ֵ�������������ͨ�� new ������ö�ٶ���
5. ƽ��ʹ��ö��ʵ��ʱ������ͨ��EnumClass.variable��ʽ������

�ο� EnumTest ʾ������


```
	public static void main(String[] args)
	{
		//����ö���඼��һ��values���������ظ�ö���������ʵ��
		for (SeasonEnum s : SeasonEnum.values())
		{
			System.out.println(s);
		}
		//ƽ��ʹ��ö��ʵ��ʱ��
		//����ͨ��EnumClass.variable��ʽ������
		new EnumTest().judge(SeasonEnum.SPRING);
	}
```



#### ��������������


![](https://github.com/SuperSurfing/JAVA_Learning_Notes/blob/master/Crazy_JAVA/Images/status.png?raw=true)

��һ����Ҫ���⡰�������������ա��Ļ��ƣ�Ҳ��̫��˽⼴�ɡ�


#### JAR

JAR - Java Archive File������һ��ѹ���ļ����볣���� zip �ļ����ݣ�ͨ������Ϊ JAR ����

JAR ��һ��ͨ�� jar ����ѹ�����ɣ�������ӵ� CLASSPATH ��JVM �ܹ����ڴ����Զ���ѹ��Ŀ¼����  

6.12 �ڻ������� jar ����Ļ����÷�����Ҳ�ǻ��� Linux ����֮һ����Ҫע����ǣ������JAVA���塷���� Windows ��������ʾ�ģ���׼ Linux ����Ӧ���� options ǰ��ӡ�-����   




### CH7-CH10

#### System_and_Runtime

##### Scanner

7.1 �ڡ����û���������Ҫ�����ˡ������в������� [Scanner](https://docs.oracle.com/javase/8/docs/api/) ����÷���Scanner �ǳ�ǿ�󣬿��Զ��������룬Ҳ���Զ��ļ���  


##### Java �� C ����ӿ�

7.2.1 ���ڽ��� System ���ʱ�򣬽�����Java ͨ������ native methods ȥ���� C ��̬���ӿ�Ľӿڵķ�����  

##### System ��

> System �����ǰ JAVA ���������ƽ̨�������ܴ��� System ���ʵ����ֻ�ܵ��������෽�������Ա��


##### Runtime ��

> Runtime ����� Java ���������ʱ������ÿ�� Java ������һ����֮��Ӧ�� Runtime ʵ����

ͨ�� procexp.exe ���Թ۲쵽��û��һ�� Java ���򣬾ͻ��´���һ�� java.exe ���̡�

> Runtime ���Ե�������һ�����������в���ϵͳ�������exec() 


#### ������

7.3 �ڽ����˳��õ��࣬������Object, String, StringBuffer, StringBuilder, Math, Random, BigDecimal����һ�ڵ�ѧϰ������࿴ʾ�����룬��Դ�����Ҹо���  


Object �� root �࣬String �ǲ��ɱ��ࣨimmutable class)��StringBuffer �ǿɱ���࣬������ҪתΪ String��StringBuilder ���̰߳�ȫ�ġ�  

Math �ṩ��������ѧ���㣬Random �������ɸ������͵�����������������ͣ���

BigDeciaml �ṩ���߾��ȵĸ������㣨תΪ�ַ����������黹��װ��һ�� Arith ��ר�ø������㡣  


7.4 �ڽ��� JAVA ��ʱ��������࣬���� Date ��Ƚ��ϣ������������ Calendar �൱���ӣ�Ҳ�����á����ѡ�������� java.time ���е��ࡣ

7.5 ����Ҫ���ܡ�������ʽ������Ҫ�� Pattern �� Matcher �����࣬���� String ��ʹ�á�


```
// ��һ���ַ�����������ʽ������� Pattern ����
Pattern p = Pattern.compile("a*b");

// ʹ�� Pattern ������ Matcher ����
Matcher m = p.matcher("aaaaab");

// ���� Matcher ����� matches ����
boolean b = m.matches();
```

��� Pattern ��ʹ��һ�Σ�����ֱ�ӵ���̬������

```
boolean b = Pattern.matches("a*b", "aaaaab");
```

��Ҫ������� Matcher ����� find ������ group �������÷���

```
public class FindGroup 
{ 
	public static void main(String[] args)
	{
		//����һ��Pattern���󣬲���������һ��Matcher����
		Matcher m = Pattern.compile("\\w+") 
			.matcher("Java is very easy!"); 
		while(m.find())
		{
			System.out.println(m.group()); 
		}
		int i = 0;
		while(m.find(i))
		{ 
			System.out.print(m.group() + "\t"); 
			i++; 
		}
	}
}
```

��һ��ѭ���ᰴ��ϸ�����Ƚ���ƥ��ͷ��ࡣ



#### ���ʻ����ʽ��

I18N - Internationalization

L10N - Localization �����ػ���

> һ�����ʻ�֧�ֺܺõ�Ӧ�ã��ڲ�ͬ������ʹ��ʱ������ֱ������Ե���ʾ��

L10N ����� OS �� Location/Region ���á�

##### ���ʻ��ķ���

JAVA ����Ĺ��ʻ������ڡ���Դ�ļ�����������Դ�ļ��������� key-value ��ʽ�ġ�  

> Java ������ʻ��Ĺؼ����� ResourceBundle �� Locale ��ResourceBundle ���ݲ�ͬ�� Locale ����������Դ�ļ����ٸ���ָ���� key ȡ���Ѽ���������Դ�ļ��е��ַ�����

```
public class Hello
{
	public static void main(String[] args)
	{
		//ȡ��ϵͳĬ�ϵĹ���/���Ի���
		Locale myLocale = Locale.getDefault();
		
		//����ָ������/���Ի���������Դ�ļ�
		ResourceBundle bundle = ResourceBundle
			.getBundle("mess" , myLocale);
			
		//��ӡ����Դ�ļ���ȡ�õ���Ϣ
		System.out.println(bundle.getString("hello"));
	}
}
```


##### ��ռλ�����ַ���

MessageFormat �����ռλ�����ַ���

```
		//����Locale����������Դ
		ResourceBundle bundle = ResourceBundle
			.getBundle("myMess" , currentLocale);
		//ȡ���Ѽ��ص�������Դ�ļ���msg��Ӧ��Ϣ
		String msg = bundle.getString("msg");
		//ʹ��MessageFormatΪ��ռλ�����ַ����������
		System.out.println(MessageFormat.format(msg
			, "yeeku" , new Date()));
```

���� MessageFormat ������ NumberFormat �� DateFormat �����Ƿֱ�ʵ����ֵ���������ַ���֮��Ļ�ת



##### ʹ�����ļ�������Դ�ļ�

```
public class myMess_zh_CN extends ListResourceBundle
{
	//������Դ
	private final Object myData[][]=
	{
		{"msg","{0}����ã������������{1}"}
	};
	//��д����getContents()
	public Object[][] getContents()
	{
		//�÷���������Դ��key-value��
		return myData;
	}
}
```

ϵͳ�������� class �ļ������� properies �ļ���










