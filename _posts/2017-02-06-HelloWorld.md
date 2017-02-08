---
layout: post
title: “Hello World”讲解
categories: [blog ]
tags:
description: I'll come in the future
header-img: "img/yun.jpg"
---

# #前言

前两节([第一节](https://younnng.github.io/blog/And-future-dialogue-JAVA.html)、[第二节](https://younnng.github.io/blog/JAVA-%E6%B3%A8%E9%87%8A.html))反复的提到了一段代码，“Hello World”,代码如下：

    1.public class HelloWorld{
    2.
    3.   public static void main(String [] args){
    4.   
    5.      System.out.println("Hello World !");
    6.      
    7.   }
    8.}   

这段代码中涉及到了很多的JAVA关键字，还有一些标识符，接下来就位大家一一讲解。

### JAVA中的关键字

关键字就是，SUN的程序员在开发JAVA语言的时候定义的一些具有特殊含义的字符序列。

就HelloWorld这段代码而言，里面的关键字就有：


1. public，公开的；
2. class，类；
3. static，静态的；
4. void，无返回值类型；


>  1. public class HelloWorld{} 就是一个公开的类，类名就是HelloWorld了，当然类名是与文件名一致的。
>  
>  2. public static void main(String [] args){}是一个主方法，是这个程序的入口，是固定的写法，关于static、void今后在为大家讲解，现在只需知道怎么写就行了。


这些都是关键字，当然还有许多关键字这段代码里面没有，这里配个图：

<center>
    <p><img src="http://wx1.sinaimg.cn/mw690/0065PbKCgy1fciyguhwy1j30j609ota4.jpg" align="center"></p>
</center>

### JAVA中的标识符

标识符，通俗的来讲，整个JAVA源文件中，自己可以命名的地方，统一称之为标识符。

标识符的特点：

1. 标识符是由字母、数字、下划线“_”和美元符号“$”构成；
2. 标识符`不能`以数字开头；
3. 关键字`不能`作为标识符；
4. 标识符区分大小写；
5. 标识符长度不做限制，但最好“见名知意”；
6. 标识符可以标识类名、变量名、接口名、方法名。


> 在“Hello World”这段代码中，HelloWorld就是一个标识符，因为他是类的名字，main也是一个标识符，因为他是方法的名字。


举个例子：

| 合法标识符   | 非法标识符    |
| :---------: | :---------: |
| HelloWorld  | Hello World |
| _Markdown   | 1Markdown   |
| public1     | String      |
| $class      | @class      |


### 关于public class和class的区别

在Hello World中可以定义一个公开的类“HelloWorld”，那么能否直接使用class直接定义呢？尝试一下：


    1.class HelloWorld{
    2.
    3.   public static void main(String [] args){
    4.   
    5.      System.out.println("Hello World !");
    6.      
    7.   }
    8.}

答案是肯定的，可以运行：

<center>
    <p><img src="http://wx4.sinaimg.cn/mw690/0065PbKCgy1fch1xl1l8bj30l50dxwu8.jpg" align="center"></p>
</center>

那么，一个JAVA源文件中能否有多个public class或者多个class呢？
先写两段代码测试一下，这段代码没有实际意义：

     1.public class A{}
     2.   class B{}
     3.     class C{}
     4.       class D{}
     5.         class E{}

运行结果如下：

<center>
    <p><img src="http://wx3.sinaimg.cn/mw690/0065PbKCgy1fch1xmyprtj30tk0g14iu.jpg" align="center"></p>
</center>

再来看看能否存在多个public class能否运行：


    1.public class F{}
    2.   public class G{}

运行结果如下：

<center>
    <p><img src="http://wx1.sinaimg.cn/mw690/0065PbKCgy1fch1xnvtq9j30tz0h2dt2.jpg" align="center"></p>
</center>

所以，我们可以得到一下结论：

1. 在一个.java源文件中，只能定义`一个`public class;
2. 在一个.java源文件中，可以定义多个class，并且编译时可以生成对应的.class字节码文件；
3. 在一个.java源文件中，可以没有public的class


>下节介绍《JAVA中的变量以及数据类型》loading... 
>okey,Gimme five~


