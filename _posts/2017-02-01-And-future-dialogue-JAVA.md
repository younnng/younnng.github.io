---
layout: post
title: And future dialogue--JAVA
categories: [blog ]
tags:
description: I'll come in the future
header-img: "img/yun.jpg"
---
# #前言

未来，离我们很近又似乎很远。想和未来“对话”吗？Follow me...

----

## How and future dialogue?

科技是第一生产力，科技的发展离不开程序，程序离不开一条条代码，而这一条条代码就是：[计算机语言](http://baike.baidu.com/link?url=7pra7XxrUOoNcu1zilA1MD3RPr-bpxx37gsK0Eg84MAZIKLVbcnuzj98wt05rdGFz9LldlidnsomuanDdhj60XALw9Yo1GncQHUORhEXj9tedmu0o_-kfOUIVG-gxHW0mHqerAKryrFZxxFPob03eq)——和未来对话的方式。

## 关于JAVA

Java是一门面向对象的计算机编程语言，是静态面向对象编程语言的杰出代表。关于JAVA的特性，顺便简单概括一下：

* 简单性，JAVA借鉴了之前一些面向对象语言的长处（如C++）摒弃了其中许多难以理解的概念。因此说JAVA语言具有简单性；
* 自动垃圾回收，JAVA有自动垃圾回收机制，当一个对象没有任何引用的时候，Java的自动垃圾收集机制就发挥作用，自动删除这个对象所占用的空间，释放存储器以避免存储器泄漏；
* 可移植性，JAVA可以实现“一次编译，到处运行”，用户只需要在自己操作系统上下载对应的JAVA虚拟机即可；
* 面向对象，是一种对现实世界理解和抽象的方法，其核心之一就是开发者在设计软件的时候可以使用自定义的类型和关联操作；

当然，JAVA的特征和优点远远不止以上几点，在后篇会为大家详细阐述。


### 关于JDK、JRE、JVM

* JDK：全称Java Development Kit，是JAVA语言软件开发工具箱；
* JRE：全称Java Runtime Environment，是JAVA的运行时环境；
* JVM：全称Java Virtual Machine，是JAVA虚拟机；

完整的JDK可以在甲骨文官网([Oracle](http://www.oracle.com/technetwork/cn/java/javase/downloads/index-jsp-138363-zhs.html))进行下载。

### JAVA的加载与执行

<center>
    <p><img src="http://wx3.sinaimg.cn/mw690/0065PbKCgy1fcb5hc2hctj30ek0b174i.jpg" align="center"></p>
</center>

在装有JVM的机器上，运行Java程序实际是JVM加载的是由.java结尾的JAVA源文件编译后的.class字节码文件，然后将字节码文件中的指令翻译为机器码执行。

## 开始你的第一个JAVA程序

上文中已经告诉JDK的下载地址，但是编写JAVA程序单凭JDK是远远不够的，为了方便我们还需借助一下编写工具，例如[eclipse](https://www.eclipse.org/downloads/download.php?file=/oomph/epp/neon/R2a/eclipse-inst-win64.exe)、EditPlus等等。

EditPls以及其他的编写工具，大家可以去谷歌里面百度一下。

### 配置PATH环境变量

PATH是可执行文件的搜索路径，在环境变量PATH搜索路径中的文件或文件夹不需要输入完整路径即可通过“运行”打开。具体步骤图解如下：

<center>
    <p><img src="http://wx4.sinaimg.cn/mw690/0065PbKCgy1fcb8u5onqnj319u0s34qp.jpg" align="center"></p>
</center>

### 编写程序 “HelloWorld”

在桌面创建一个.TXT文件并且将文件名命名为“HelloWorld”后缀改写为.java。然后双击文件，用你安装的编写工具打开，在编写工具中输入这段代码：

    1. public class HelloWorld {
    2.    public static void main(String[] args) {
    3.	      System.out.println("HelloWorld!");
    4.	 }
    5. }

### 运行“HelloWorld”

1. win+R 打开运行，在里面输入CMD点击确定；
2. 在该文件径下输入：javac HelloWorld.java ；
3. 回车；
4. 再输入：java HelloWorld 回车运行；
5. 看看效果吧~~

图解如下：

<center>
    <p><img src="http://wx4.sinaimg.cn/mw690/0065PbKCgy1fcba3vceqkj312e0ize32.jpg" align="center"></p>
</center>

当然，你也可以直接在eclipse这样的工具中直接创建文件，直接进行控制台输出。
---


>结语，对JAVA的初步认识到此结束，后续逐步更新loaing... 
>okey,Gimme five~
