# Java基础
一个纯新手的快速入门，言简意赅，来自一个自学者的提要。参考和部分转载[http://www.runoob.com/java/java-tutorial.html]
## Java简介 
图片[]
Java 是由Sun Microsystems公司于1995年5月推出的高级程序设计语言。
Java可运行于多个平台，如Windows, Mac OS，及其他多种UNIX版本的系统。
本教程通过简单的实例将让大家更好的了解JAVA编程语言。Java语言的特点简单、解释性、面向对象、健壮、动态、高性能、多线程、分布式处理、安全性、开源、结构中立、跨平台。 3大特性  1.安全性  2.虚拟机JVM（一次编译到处运行） 3.GC垃圾回收机制
## 开发环境配置、开发工具的安装
环境配置、安装各开发工具网上教程是比较多且详细，具体可以百度或参考 [http://www.runoob.com/java/java-environment-setup.html] 

算法导论资料  https://blog.csdn.net/mao_hui_fei/article/details/83453168
Android设计模式 https://www.cnblogs.com/android-blogs/p/5530239.html
兼职网站：   taskcity： http://www.taskcity.com/
            软件商务网： www.bizsofts.com/
                        https://www.sxsoft.com/

##  基础语法
1. 编写Java程序时，应注意以下几点：
 大小写敏感：Java是大小写敏感的，这就意味着标识符Hello与hello是不同的。严格区分大小写
 类名：对于所有的类来说，类名的首字母应该大写。如果类名由若干单词组成，那么每个单词的首字母应该大写，例如 MyFirstJavaClass 。
 方法名：所有的方法名都应该以小写字母开头。如果方法名含有若干单词，则后面的每个单词首字母大写。
 源文件名：源文件名必须和类名相同。当保存文件的时候，你应该使用类名作为文件名保存（切记Java是大小写敏感的），文件名的后缀为.java。（如果文件名和类     名不相同则会导致编译错误）。
 主方法入口：所有的Java 程序由public static void main(String []args)方法开始执行。

1. 标识符 可参考阿里巴巴Java开发手册（公开版）有需要自行百度
所有的标识符都应该以字母（A-Z或者a-z）,美元符（$）、或者下划线（_）开始
首字符之后可以是字母（A-Z或者a-z）,美元符（$）、下划线（_）或数字的任何字符组合
关键字不能用作标识符
标识符是大小写敏感的
合法标识符举例：age、$salary、_value、__1_value
非法标识符举例：123abc、-salary

1. 枚举
   Java 5.0引入了枚举，枚举限制变量只能是预先设定好的值。使用枚举可以减少代码中的bug。
   例如，我们为果汁店设计一个程序，它将限制果汁为小杯、中杯、大杯。这就意味着它不允许顾客点除了这三种尺寸外的果汁。
   

## 对象和类
1. 一个Java程序可以认为是一系列对象的集合，而这些对象通过调用彼此的方法来协同工作。下面简要介绍下类、对象、方法和实例变量的概念。
1. 对象：对象是类的一个实例，有状态和行为。例如，一条狗是一个对象，它的状态有：颜色、名字、品种；行为有：摇尾巴、叫、吃等。
1. 类：类是一个模板，它描述一类对象的行为和状态。
1. 方法：方法就是行为，一个类可以有很多方法。逻辑运算、数据修改以及所有动作都是在方法中完成的。
1. 实例变量：每个对象都有独特的实例变量，对象的状态由这些实例变量的值决定。

## 基本数据类类型 （存储在栈区）
8大基本类型  byte1个字节  short2个字节  int4个字节   long8个字节  char1个字节   float4个字节  double8个字节  boolean1个字节 
引用类型 引用的为对象
## 变量类型
 ### 局部变量 Java中所有变量使用前必须先声明 type identifier [ = value][, identifier [= value] ...] ;
 局部变量声明在方法、构造方法或者语句块中；
 局部变量在方法、构造方法、或者语句块被执行的时候创建，当它们执行完成后，变量将会被销毁；
 访问修饰符不能用于局部变量；
 局部变量只在声明它的方法、构造方法或者语句块中可见；
 局部变量是在栈上分配的。
 局部变量没有默认值，所以局部变量被声明后，必须经过初始化，才可以使用。
 
 ### 实例变量 （成员变量）
 实例变量声明在一个类中，但在方法、构造方法和语句块之外；
 当一个对象被实例化之后，每个实例变量的值就跟着确定；
 实例变量在对象创建的时候创建，在对象被销毁的时候销毁；
 实例变量的值应该至少被一个方法、构造方法或者语句块引用，使得外部能够通过这些方式获取实例变量信息；
 实例变量可以声明在使用前或者使用后；
 访问修饰符可以修饰实例变量；
 实例变量对于类中的方法、构造方法或者语句块是可见的。一般情况下应该把实例变量设为私有。通过使用访问修饰符可以使实例变量对子类可见；
 实例变量具有默认值。数值型变量的默认值是0，布尔型变量的默认值是false，引用类型变量的默认值是null。变量的值可以在声明时指定，也可以在构造方法中指定；
 实例变量可以直接通过变量名访问。但在静态方法以及其他类中，就应该使用完全限定名：ObejectReference.VariableName。
 
 ### 类变量（静态变量）
 类变量也称为静态变量，在类中以 static 关键字声明，但必须在方法之外。
 无论一个类创建了多少个对象，类只拥有类变量的一份拷贝。
 静态变量除了被声明为常量外很少使用。常量是指声明为public/private，final和static类型的变量。常量初始化后不可改变。
 静态变量储存在静态存储区。经常被声明为常量，很少单独使用static声明变量。
 静态变量在第一次被访问时创建，在程序结束时销毁。
 与实例变量具有相似的可见性。但为了对类的使用者可见，大多数静态变量声明为public类型。
 默认值和实例变量相似。数值型变量默认值是0，布尔型默认值是false，引用类型默认值是null。变量的值可以在声明的时候指定，也可以在构造方法中指定。此外，静   态变量还可以在静态语句块中初始化。
 静态变量可以通过：ClassName.VariableName的方式访问。
 类变量被声明为public static final类型时，类变量名称一般建议使用大写字母。如果静态变量不是public和final类型，其命名方式与实例变量以及局部变量的命名   方式一致。


## 修饰符
访问控制修饰符 : default, public , protected, private
Java中，可以使用访问控制符来保护对类、变量、方法和构造方法的访问。Java 支持 4 种不同的访问权限。
default (即缺省，什么也不写）: 在同一包内可见，不使用任何修饰符。使用对象：类、接口、变量、方法。
private : 在同一类内可见。使用对象：变量、方法。 注意：不能修饰类（外部类）
私有访问修饰符-private
私有访问修饰符是最严格的访问级别，所以被声明为 private 的方法、变量和构造方法只能被所属类访问，并且类和接口不能声明为 private。
声明为私有访问类型的变量只能通过类中公共的 getter 方法被外部类访问。
Private 访问修饰符的使用主要用来隐藏类的实现细节和保护类的数据。

public : 对所有类可见。使用对象：类、接口、变量、方法
被声明为 public 的类、方法、构造方法和接口能够被任何其他类访问。 
如果几个相互访问的 public 类分布在不同的包中，则需要导入相应 public 类所在的包。由于类的继承性，类所有的公有方法和变量都能被其子类继承。 

protected : 对同一包内的类和所有子类可见。使用对象：变量、方法。 注意：不能修饰类（外部类）。
rotected 需要从以下两个点来分析说明：
子类与基类在同一包中：被声明为 protected 的变量、方法和构造器能被同一个包中的任何其他类访问；
子类与基类不在同一包中：那么在子类中，子类实例可以访问其从基类继承而来的 protected 方法，而不能访问基类实例的protected方法。
protected 可以修饰数据成员，构造方法，方法成员，不能修饰类（内部类除外）。

非访问控制修饰符 : static，final, abstract, static, synchronized
为了实现一些其他的功能，Java 也提供了许多非访问修饰符。
static 修饰符，用来修饰类方法和类变量。
final 修饰符，用来修饰类、方法和变量，final 修饰的类不能够被继承，修饰的方法不能被继承类重新定义，修饰的变量为常量，是不可修改的。
abstract 修饰符，用来创建抽象类和抽象方法。
synchronized 和 volatile 修饰符，主要用于线程的编程。

static 修饰符，用来修饰类方法和类变量。
final 修饰符，用来修饰类、方法和变量，final 修饰的类不能够被继承，修饰的方法不能被继承类重新定义，修饰的变量为常量，是不可修改的。
abstract 修饰符，用来创建抽象类和抽象方法。
synchronized 和 volatile 修饰符，主要用于线程的编程。
static 修饰符
静态变量：
static 关键字用来声明独立于对象的静态变量，无论一个类实例化多少对象，它的静态变量只有一份拷贝。 静态变量也被称为类变量。局部变量不能被声明为 static 变量。 
静态方法：
static 关键字用来声明独立于对象的静态方法。静态方法不能使用类的非静态变量。静态方法从参数列表得到数据，然后计算这些数据。 
对类变量和方法的访问可以直接使用 classname.variablename 和 classname.methodname 的方式访问。 
如下例所示，static修饰符用来创建类方法和类变量。
public class InstanceCounter {
   private static int numInstances = 0;
   protected static int getCount() {
      return numInstances;
   }
 
   private static void addInstance() {
      numInstances++;
   }
 
   InstanceCounter() {
      InstanceCounter.addInstance();
   }
 
   public static void main(String[] arguments) {
      System.out.println("Starting with " +
      InstanceCounter.getCount() + " instances");
      for (int i = 0; i < 500; ++i){
         new InstanceCounter();
          }
      System.out.println("Created " +
      InstanceCounter.getCount() + " instances");
   }
}
以上实例运行编辑结果如下:
Starting with 0 instances
Created 500 instances
final 修饰符
final 变量：
final 表示"最后的、最终的"含义，变量一旦赋值后，不能被重新赋值。被 final 修饰的实例变量必须显式指定初始值。
final 修饰符通常和 static 修饰符一起使用来创建类常量。
实例
public class Test{
  final int value = 10;
  // 下面是声明常量的实例
  public static final int BOXWIDTH = 6;
  static final String TITLE = "Manager";
 
  public void changeValue(){
     value = 12; //将输出一个错误
  }
}
final 方法
类中的 final 方法可以被子类继承，但是不能被子类修改。
声明 final 方法的主要目的是防止该方法的内容被修改。
如下所示，使用 final 修饰符声明方法。
public class Test{
    public final void changeName(){
       // 方法体
    }
}
final 类
final 类不能被继承，没有类能够继承 final 类的任何特性。
实例
public final class Test {
   // 类体
}
abstract 修饰符
抽象类：
抽象类不能用来实例化对象，声明抽象类的唯一目的是为了将来对该类进行扩充。 
一个类不能同时被 abstract 和 final 修饰。如果一个类包含抽象方法，那么该类一定要声明为抽象类，否则将出现编译错误。 
抽象类可以包含抽象方法和非抽象方法。 
实例
abstract class Caravan{
   private double price;
   private String model;
   private String year;
   public abstract void goFast(); //抽象方法
   public abstract void changeColor();
}
抽象方法
抽象方法是一种没有任何实现的方法，该方法的的具体实现由子类提供。
抽象方法不能被声明成 final 和 static。 
任何继承抽象类的子类必须实现父类的所有抽象方法，除非该子类也是抽象类。 
如果一个类包含若干个抽象方法，那么该类必须声明为抽象类。抽象类可以不包含抽象方法。 
抽象方法的声明以分号结尾，例如：public abstract sample();。 
实例
public abstract class SuperClass{
    abstract void m(); //抽象方法
}
 
class SubClass extends SuperClass{
     //实现抽象方法
      void m(){
          .........
      }
}
synchronized 修饰符
synchronized 关键字声明的方法同一时间只能被一个线程访问。synchronized 修饰符可以应用于四个访问修饰符。 
实例
public synchronized void showDetails(){
.......
}
transient 修饰符
序列化的对象包含被 transient 修饰的实例变量时，java 虚拟机(JVM)跳过该特定的变量。 
该修饰符包含在定义变量的语句中，用来预处理类和变量的数据类型。 
实例
public transient int limit = 55;   // 不会持久化
public int b; // 持久化
volatile 修饰符
volatile 修饰的成员变量在每次被线程访问时，都强制从共享内存中重新读取该成员变量的值。而且，当成员变量发生变化时，会强制线程将变化值回写到共享内存。这样在任何时刻，两个不同的线程总是看到某个成员变量的同一个值。
一个 volatile 对象引用可能是 null。 
实例
public class MyRunnable implements Runnable
{
    private volatile boolean active;
    public void run()
    {
        active = true;
        while (active) // 第一行
        {
            // 代码
        }
    }
    public void stop()
    {
        active = false; // 第二行
    }
}
通常情况下，在一个线程调用 run() 方法（在 Runnable 开启的线程），在另一个线程调用 stop() 方法。 如果 第一行 中缓冲区的 active 值被使用，那么在 第二行 的 active 值为 false 时循环不会停止。 
但是以上代码中我们使用了 volatile 修饰 active，所以该循环会停止。


## 运算符
计算机的最基本用途之一就是执行数学运算，作为一门计算机语言，Java也提供了一套丰富的运算符来操纵变量。我们可以把运算符分成以下几组：
算术运算符
+
加法 - 相加运算符两侧的值
A + B 等于 30
-
减法 - 左操作数减去右操作数
A – B 等于 -10
*
乘法 - 相乘操作符两侧的值
A * B等于200
/
除法 - 左操作数除以右操作数
B / A等于2
％
取余 - 左操作数除以右操作数的余数
B%A等于0
++
自增: 操作数的值增加1
B++ 或 ++B 等于 21（区别详见下文）
--
自减: 操作数的值减少1
B-- 或 --B 等于 19（区别详见下文）
1、自增（++）自减（--）运算符是一种特殊的算术运算符，在算术运算符中需要两个操作数来进行运算，而自增自减运算符是一个操作数。

关系运算符
==
检查如果两个操作数的值是否相等，如果相等则条件为真。
（A == B）为假。
!=
检查如果两个操作数的值是否相等，如果值不相等则条件为真。
(A != B) 为真。
> 
检查左操作数的值是否大于右操作数的值，如果是那么条件为真。
（A> B）为假。
< 
检查左操作数的值是否小于右操作数的值，如果是那么条件为真。
（A <B）为真。
>=
检查左操作数的值是否大于或等于右操作数的值，如果是那么条件为真。
（A> = B）为假。
<=
检查左操作数的值是否小于或等于右操作数的值，如果是那么条件为真。
（A <= B）为真。

位运算符
＆
如果相对应位都是1，则结果为1，否则为0
（A＆B），得到12，即0000 1100 </br>
|
如果相对应位都是0，则结果为0，否则为1
（A | B）得到61，即 0011 1101 </br>
^
如果相对应位值相同，则结果为0，否则为1
（A ^ B）得到49，即 0011 0001 </br>
〜
按位取反运算符翻转操作数的每一位，即0变成1，1变成0。
（〜A）得到-61，即1100 0011 </br>
<< 
按位左移运算符。左操作数按位左移右操作数指定的位数。
A << 2得到240，即 1111 0000 </br>
>> 
按位右移运算符。左操作数按位右移右操作数指定的位数。
A >> 2得到15即 1111 </br>
>>> 
按位右移补零操作符。左操作数的值按右操作数指定的位数右移，移动得到的空位以零填充。
A>>>2得到15即0000 1111 </br>

逻辑运算符
&&称为逻辑与运算符。当且仅当两个操作数都为真，条件才为真。
（A && B）为假。 </br> 
| |称为逻辑或操作符。如果任何两个操作数任何一个为真，条件为真。
（A | | B）为真。</br>
！称为逻辑非运算符。用来反转操作数的逻辑状态。如果条件为true，则逻辑非运算符将得到false。
！（A && B）为真。</br>
    短路逻辑运算符

赋值运算符
=
简单的赋值运算符，将右操作数的值赋给左侧操作数
C = A + B将把A + B得到的值赋给C
+ =
加和赋值操作符，它把左操作数和右操作数相加赋值给左操作数
C + = A等价于C = C + A
- =
减和赋值操作符，它把左操作数和右操作数相减赋值给左操作数
C - = A等价于C = C -
 A
* =
乘和赋值操作符，它把左操作数和右操作数相乘赋值给左操作数
C * = A等价于C = C * A
/ =
除和赋值操作符，它把左操作数和右操作数相除赋值给左操作数
C / = A等价于C = C / A
（％）=
取模和赋值操作符，它把左操作数和右操作数取模后赋值给左操作数
C％= A等价于C = C％A
<< =
左移位赋值运算符
C << = 2等价于C = C << 2
>> =
右移位赋值运算符
C >> = 2等价于C = C >> 2
＆=
按位与赋值运算符
C＆= 2等价于C = C＆2
^ =
按位异或赋值操作符
C ^ = 2等价于C = C ^ 2
| =
按位或赋值操作符
C | = 2等价于C = C | 2

其他运算符
条件运算符也被称为三元运算符。该运算符有3个操作数，并且需要判断布尔表达式的值。该运算符的主要是决定哪个值应该赋值给变量。
variable x = (expression) ? value if true : value if false

instanceof 运算符
该运算符用于操作对象实例，检查该对象是否是一个特定类型（类类型或接口类型）。
instanceof运算符使用格式如下：
( Object reference variable ) instanceof  (class/interface type）

## 循环结构
顺序结构的程序语句只能被执行一次。如果您想要同样的操作执行多次,，就需要使用循环结构。 
Java中有三种主要的循环结构：
while 循环
do…while 循环
for 循环
Java 增强 for 循环
Java5 引入了一种主要用于数组的增强型 for 循环。
Java 增强 for 循环语法格式如下:
for(声明语句 : 表达式)
{
   //代码句子
}
声明语句：声明新的局部变量，该变量的类型必须和数组元素的类型匹配。其作用域限定在循环语句块，其值与此时数组元素的值相等。 
表达式：表达式是要访问的数组名，或者是返回值为数组的方法。

break 关键字
break 主要用在循环语句或者 switch 语句中，用来跳出整个语句块。 
break 跳出最里层的循环，并且继续执行该循环下面的语句。

continue 关键字
continue 适用于任何循环控制结构中。作用是让程序立刻跳转到下一次循环的迭代。 
在 for 循环中，continue 语句使程序立即跳转到更新语句。 
在 while 或者 do…while 循环中，程序立即跳转到布尔表达式的判断语句。

## 条件语句
一个 if 语句包含一个布尔表达式和一条或多条语句。
if 语句后面可以跟 else if…else 语句，这种语句可以检测到多种可能的情况。

使用 if，else if，else 语句的时候，需要注意下面几点：

if 语句至多有 1 个 else 语句，else 语句在所有的 else if 语句之后。
if 语句可以有若干个 else if 语句，它们必须在 else 语句之前。
一旦其中一个 else if 语句检测为 true，其他的 else if 以及 else 语句都将跳过执行。

switch case 语句有如下规则：
switch 语句中的变量类型可以是： byte、short、int 或者 char。从 Java SE 7 开始，switch 支持字符串 String 类型了，同时 case 标签必须为字符串常量或字面量。
switch 语句可以拥有多个 case 语句。每个 case 后面跟一个要比较的值和冒号。
case 语句中的值的数据类型必须与变量的数据类型相同，而且只能是常量或者字面常量。
当变量的值与 case 语句的值相等时，那么 case 语句之后的语句开始执行，直到 break 语句出现才会跳出 switch 语句。
当遇到 break 语句时，switch 语句终止。程序跳转到 switch 语句后面的语句执行。case 语句不必须要包含 break 语句。如果没有 break 语句出现，程序会继续执行下一条 case 语句，直到出现 break 语句。
switch 语句可以包含一个 default 分支，该分支一般是 switch 语句的最后一个分支（可以在任何位置，但建议在最后一个）。default 在没有 case 语句的值和变量值相等的时候执行。default 分支不需要 break 语句。
switch case 执行时，一定会先进行匹配，匹配成功返回当前 case 的值，再根据是否有 break，判断是否继续输出，或是跳出判断。


## 数组 
Java 语言中提供的数组是用来存储固定大小的同类型元素。

数组索引是在栈上，根据索引指向堆区的内存（）
数组是储存在堆上的对象，可以保存多个同类型变量。
空指针异常
数组索引越界
二维数组
## 日期和时间
Java.util包提供了Date类来封装日期和时间java.util 包提供了 Date 类来封装当前的日期和时间。 Date 类提供两个构造函数来实例化 Date 对象。

第一个构造函数使用当前日期和时间来初始化对象。

Date( )
第二个构造函数接收一个参数，该参数是从1970年1月1日起的毫秒数。

Date(long millisec)

##  正则表达式
Java 正则表达式
正则表达式定义了字符串的模式。
正则表达式可以用来搜索、编辑或处理文本。
正则表达式并不仅限于某一种语言，但是在每种语言中有细微的差别。

## Java 流(Stream)、文件(File)和IO
Java.io 包几乎包含了所有操作输入、输出需要的类。所有这些流类代表了输入源和输出目标。

Java.io 包中的流支持很多种格式，比如：基本类型、对象、本地化字符集等等。

一个流可以理解为一个数据的序列。输入流表示从一个源读取数据，输出流表示向一个目标写数据。

Java 为 I/O 提供了强大的而灵活的支持，使其更广泛地应用到文件传输和网络编程中。
Java 的控制台输入由 System.in 完成。

为了获得一个绑定到控制台的字符流，你可以把 System.in 包装在一个 BufferedReader 对象中来创建一个字符流。
下面是创建 BufferedReader 的基本语法：
BufferedReader br = new BufferedReader(new InputStreamReader(System.in));
                      
## 异常处理
## 小技巧
1. 注释
   2种注释方式   //   单行注释  ;  /* string body */ 多行注释  /** string body*/  说明注释允许你在程序中嵌入关于程序的信息。你可以使用 javadoc 工具软件来生成信息，并输出到HTML文件中。具体参考[https://jingyan.baidu.com/article/eb9f7b6d4b1f6a869364e83d.html]
说明注释，使你更加方便的记录你的程序信息。
   空行 Java是无视空行 为了代码的优雅清爽 建议是适当使用
   /** 方法的头上 回车
   ##函数注释参数信息 
   1.Android Studio ->File -> Setting -> Keymap ->发现框输入comment -> 选择Other的Fix doc comment 
   选择 Add keyboard shortcut 添加你自己喜欢的快捷方式（快捷键） 将鼠标光标放置到你想要添加方法注释的
   方法前,按下你自己设置的快捷方式. 就自动生成了方法注释了. 

简而言之：框架是大智慧，用来对软件设计进行分工；设计模式是小技巧，对具体问题提出解决方案，以提高代码复用率，降低耦合度。
   
# 面向对象

## 继承
继承的概念（Java为单根继承）
继承是java面向对象编程技术的一块基石，因为它允许创建分等级层次的类。
继承就是子类继承父类的特征和行为，使得子类对象（实例）具有父类的实例域和方法，或子类从父类继承方法，使得子类具有父类相同的行为。 

## 重载和重写
## 多态
## 抽象
## 封装
## 接口
## 包

# Java高级
## 数据结构
## 集合框架
## 泛型
## 序列化
## 网络编程
## 多线程
## 数据库
