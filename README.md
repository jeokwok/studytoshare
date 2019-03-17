# Java基础
一个纯新手的快速入门，言简意赅，来自一个自学者的提要。参考和部分转载[http://www.runoob.com/java/java-tutorial.html]
## Java简介 
图片[]
Java 是由Sun Microsystems公司于1995年5月推出的高级程序设计语言。
Java可运行于多个平台，如Windows, Mac OS，及其他多种UNIX版本的系统。
本教程通过简单的实例将让大家更好的了解JAVA编程语言。Java语言的特点简单、解释性、面向对象、健壮、动态、高性能、多线程、分布式处理、安全性、开源、结构中立、跨平台。 3大特性  1.安全性  2.虚拟机JVM（一次编译到处运行） 3.GC垃圾回收机制
## 开发环境配置、开发工具的安装
环境配置、安装各开发工具网上教程是比较多且详细，具体可以百度或参考 [http://www.runoob.com/java/java-environment-setup.html] 

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

## 基本数据类类型
8大基本类型  byte1个字节  short2个字节  int4个字节   long8个字节  char1个字节   float4个字节  double8个字节  boolean1个字节 
引用类型 引用的为对象
## 变量类型
 局部变量
 类变量（静态变量）
 成员变量（非静态变量）

## 修饰符
访问控制修饰符 : default, public , protected, private
非访问控制修饰符 : final, abstract, static, synchronized
## 运算符
## 循环结构
## 条件语句
## 数组
数组是储存在堆上的对象，可以保存多个同类型变量。

## 异常处理
## 小技巧
1. 注释
   2种注释方式   //   单行注释  ;  /* string body */ 多行注释   
   空行 Java是无视空行 为了代码的优雅清爽 建议是适当使用
   /** 方法的头上 回车
   ##函数注释参数信息 
   1.Android Studio ->File -> Setting -> Keymap ->发现框输入comment -> 选择Other的Fix doc comment 
   选择 Add keyboard shortcut 添加你自己喜欢的快捷方式（快捷键） 将鼠标光标放置到你想要添加方法注释的
   方法前,按下你自己设置的快捷方式. 就自动生成了方法注释了. 

   
# 面向对象
## 继承
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

## README 
1. Hello Git! Git Bash 命令


##JSON 获取部分中数组的数据
public static void jsonToBean(String data) {
try {
JSONArray array = new JSONArray(data);//将json字符串转成json数组

for (int i = 0; i < array.length(); i++) {//循环json数组
JSONObject ob = (JSONObject) array.get(i);//得到json对象
String name= ob.getString("name");//name这里是列名称，获取json对象中列名为name的值
System.out.print(name);//输出name
} catch (JSONException e) {
}
} 

视频网址 [http://m.tlyy.tv/movie.html]

