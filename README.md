# Java基础
一个纯新手的快速入门，言简意赅，来自一个自学者的提要。
## Java简介 

Java 是由Sun Microsystems公司于1995年5月推出的高级程序设计语言。
Java可运行于多个平台，如Windows, Mac OS，及其他多种UNIX版本的系统。
本教程通过简单的实例将让大家更好的了解JAVA编程语言。

##  基础语法
1. 一个Java程序可以认为是一系列对象的集合，而这些对象通过调用彼此的方法来协同工作。下面简要介绍下类、对象、方法和实例变量的概念。
1. 对象：对象是类的一个实例，有状态和行为。例如，一条狗是一个对象，它的状态有：颜色、名字、品种；行为有：摇尾巴、叫、吃等。
1. 类：类是一个模板，它描述一类对象的行为和状态。
1. 方法：方法就是行为，一个类可以有很多方法。逻辑运算、数据修改以及所有动作都是在方法中完成的。
1. 实例变量：每个对象都有独特的实例变量，对象的状态由这些实例变量的值决定。

## 小技巧

## README 
1. Hello Git! Git Bash 命令

/** 方法的头上 回车
##函数注释参数信息 
1.Android Studio ->File -> Setting -> Keymap ->发现框输入comment -> 选择Other的Fix doc comment 
选择 Add keyboard shortcut 添加你自己喜欢的快捷方式（快捷键） 将鼠标光标放置到你想要添加方法注释的
方法前,按下你自己设置的快捷方式. 就自动生成了方法注释了. 

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

