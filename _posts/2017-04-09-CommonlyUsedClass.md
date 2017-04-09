---
layout: post
title: JAVA中的常用类
categories: [blog ]
tags:
description: I'll come in the future
header-img: "img/yun.jpg"
---

## 前言

为啥没有面向对象的博文？面向对象就是：封装、继承、多态，所以没有O(∩_∩)O哈哈~


### JAVA中的常用类

#### String类及其中的常用方法

String代表字符串，是引用类型。Java程序中的所有字符串字面值都作为此类的实例实现。简而言之，在Java中只要我们用到 " "(双引号)的格式来创建的都属于String类型的对象,并且该String对象都在`对象池`中分配空间。对`象池`中的对象都是被共享的,而new出来的对象会在堆中分配空间。String对象的值一旦创建好之后，String对象的内容是不可被改变的。


看如下代码：

    1. String s1 = "Hello";
    2. String s2 = "Hello";
    3. String s3 = new String("Hello");
    4. String s4 = new String("Hello");
    5. // == 对于引用类型来说比较的是两个引用的地址是否相同，
    6. //也就是两个引用是否指向同一对象
    7. System.out.println(s1 == s2);//true
    8. System.out.println(s3 == s4);//false
    9. System.out.println(s1 == s3);//false
    10. /*--------华丽的分割线--------*/
    11. //如下代码创建了几个String对象？(3个对象)
    12. String s5 = new String("World");
    13. String s6 = new String("World");



#### String类中的常用方法

    1. //1.charAt(int index);返回一个字符串中,指定索引出的char值
    2. String str1 = "asdghi";
    3. char ch1 = str1.charAt(2);
    4. System.out.pringtln(ch1);// d
    5. /*--------华丽的分割线--------*/
    6. 
    7. //2.codePointAt(int index);返回指定索引处的字符的Unicode编码
    8. String str2 = "HelloWorld";
    9. int i1 = str2.indexOf("d");
    10. int i2 = str2.codePointAt(i1);
    11. System.out.println(i2);// 100
    12. /*--------华丽的分割线--------*/
    13. 
    14. //3.compareTo()按字典顺序比较字符串,该方法比较时忽略长度,返回一个int值
    15. String str3 = "aa";
    16. String str4 = "b";
    17. String str5 = "ab";
    18. String str6 = "bb";
    19. System.out.pringtln(str3.compareTo(str4));//-1
    20. System.out.pringtln(str5.compareTo(str6));//-1
    21. /*--------华丽的分割线--------*/
    22. 
    23. //4.concat()用于字符串的连接
    24. String st1 = "Hello";
    25. String st2 = "World";
    26. System.out.println(st1.concat(st2));//"HelloWorld"
    27. /*--------华丽的分割线--------*/
    28. 
    29. //5.endsWith()方法测试字符串是否以指定的后缀结束,返回boolean类型的值
    30. String st3 = "HelloWorld.java";
    31. System.out.println(st3.endsWith(".java"));//true
    32. /*--------华丽的分割线--------*/
    33. 
    34. //6.equalsIgnoreCase()比较两个字符串是否相等(忽略大小写)
    35. String st4 = "abcd";
    36. String st5 = "ABcD";
    37. System.out.println(st4.equalsIgnoreCase(st5));//true
    38. /*--------华丽的分割线--------*/
    39. 
    40. //7.indexOf()在一个字符串中查找指定的字符,返回字符第一次出现的索引,没有则返回-1
    41. String st6 = "HellojavaWorldjava";
    42. System.out.println(st6.indexOf("java"));//5
    43. /*--------华丽的分割线--------*/
    44. 
    45. //8.isEmpty()测试一个字符串是否为空串,只有当该字符串的length为0的时候,返回true;
    46. String st7 = "    ";//这里有4个空格
    47. String st8  = "";
    48. System.out.println(st7.isEmpty());//false
    49. System.out.println(st8.isEmpty());//true
    50. /*--------华丽的分割线--------*/
    51. 
    52. //9.replaceAll()替换字符串中的指定字符
    53. String st9 = "我ai你";
    54. System.out.println(st9.replaceAll("ai","爱"));//"我爱你"
    55. /*--------华丽的分割线--------*/
    56. 
    57. //10.split()将一个字符串按照标记分割成一个字符串数组
    58. String s1 = "asd;zxc;qwe";
    59. String[] arr1 = s1.split(";");
    60. System.out.println(Arrays.toString(arr1));//[asd,zxc,qwe]
    61. /*--------华丽的分割线--------*/
    62. 
    63. //11.substring()从指定索引出开始截取字符串到末尾
    64. String s2 = "HelloWorld";
    65. int indexWorld1 = s2.indexOf("World");
    66. System.out.println(s2.substring(indexWorld1));//World
    67. String s3 = "HelloWorldJava";
    68. int indexWorld2 = s3.indexOf("World");
    67. System.out.println(s3.substring(indexWorld2,(indexWorld2+"World".length())));//World
    68. /*--------华丽的分割线--------*/
    69. 
    70. //12.toUppreCase()转大写,toLowerCase()转小写
    71. String s4 = "aBcDefG";
    72. s4 = s4.toUpperCase();
    73. System.out.println(s4);// ABCDEFG
    74. s4 = s4.toLowerCase();
    75. System.out.println(s4);// abcdefg
    76. /*--------华丽的分割线--------*/
    77. 
    78. //13.trim()忽略字符串前后的空格
    79. String s5 = "   abc  de   ";
    80. System.out.println(s5.trim());//"abc  de"
    81. /*--------华丽的分割线--------*/
    82. 
    83. //14.valueOf()三个字很强大!!!将引用类型或者基础类型转换成字符串
    84. int i4 = 123456;
    85. String s6 = String.valueOf(i4);
    86. System.out.println(s6);// "123456"
    87. /*--------华丽的分割线--------*/
    88. 
    89. //15.contains()当字符串含有指定字符时返回true
    90. String m = "123456789";
    91. System.out.println(m.contains("8"));//true
    92. /*--------华丽的分割线--------*/


#### StringBuffer类和StringBuilder类

StringBuffer，线程安全的可变字符序列，一个类似于String的字符串缓冲区，其底层实质也是个char[]，有自动扩容功能。但是StringBuffer速度慢StringBuilder，的功能和StringBuffer类似，但是其线程不安全，速度快。

以StringBuffer为例，介绍其功能和类里提供的常用方法

    1. StringBuffer c1 = new StringBuffer("Hello");
    2. // StringBuffer()的底层也是一个char[],并且可以自动扩容,默认容量为16
    3. // 用于字符串的拼接
    4. c1.append("World").append(".").append("java");
    5. System.out.println(c1);
    6. // 在指定位置插入数据用insert(指定位置,需要插入的数据)方法
    7. StringBuffer c2 = new StringBuffer("HelloWorld");
    8. // 在Hello的后面插入java
    9. StringBuffer temp = c2;
    10. c2 = c2.insert(5, "java");//需要插入地方的索引，插入的字符
    11. System.out.println(c2);// 不会覆盖World
    12. // 看地址有无变化
    13. System.out.println(c2 == temp);// true


#### BigDecimal类提供精确的浮点计算

    1. // BigDecimal(double dou)有一定的不可预知性,慎用,一般建议,先转化为字符串类型.
    2. // 该类有提供BigDecimal(String str)的构造方法.
    3. double dou1 = 9.111111;
    4. double dou2 = 1.111111;
    5. // 计算两者之和,用add();
	6.	BigDecimal big1 = new BigDecimal(Double.toString(dou1));
	7.	BigDecimal big2 = new BigDecimal(Double.toString(dou2));
	8.	System.out.println(big1.add(big2));// 10.222222没有丢失精度


#### DecimalFormat类用于格式化十进制的数字

    1. // 0表示该位置有数值就显示数值,没有数值就强制的显示为0
	2. // #表示该位置有数值就显示数值,没有数值就不显示.
	3. // .小数分隔符 ,数字分隔符 %后缀百分数
	4. // 用格式引用.format(数值)的方式格式化一个数值
	5.	double dou3 = 100000000.99;
	6.	DecimalFormat df1 = new DecimalFormat("000,000,000,000.000");
	7.	System.out.println(df1.format(dou3));// 000,100,000,000.990;字符串的格式
	8.	DecimalFormat df2 = new DecimalFormat("###,###,###,###.###");
	9.	String r1 = df2.format(dou3);
	10.	System.out.println(r1);// 100,000,000.99
 
#### Random类可产生随机数

    1. Random ran = new Random();
	2.	int i5 = ran.nextInt(10);// 生成0~10之间的随机数,包含0,不包括10
	3.	System.out.println(i5);

#### Date类，时间类（util中的）

    1. // util中的Date类可生成当前时间
	2.	Date da1 = new Date();
	3.	System.out.println(da1);// Sat Apr 08 21:44:03 CST 2017可读性差
	4.	// 按照指定的格式格式化现在的时间
	5.	SimpleDateFormat sdf1 = new SimpleDateFormat("yyyy年MM月dd日 HH:mm:ss SSS");
	6.	// SimpleDateFormat中提供的format()方法返回的是一个按照格式的String类型的值
	7.	String r2 = sdf1.format(da1);
	8.	System.out.println(r2);
	9.	// 自定义日期和时间,按照格式生成Date,格式不变,用parse解析字符串
	10.	String r3 = "1997年01月01日 01:01:01 000";
	12.	try {
	13.		// 该解析可能发生异常
	14.		Date da2 = sdf1.parse(r3);
	15.		System.out.println(da2);
	16.		System.out.println(sdf1.format(da2));
	17.	} catch (ParseException e) {
	18.		// TODO Auto-generated catch block
	19.		e.printStackTrace();
	20.	}


#### 包装器

基本类型对应的包装类型如下：

| 类型描述 | 关键字 | 包装类型 |
|:--------:|:--------:|:--------:|
| 字节型 | byte | Byte |
| 短整型 | short | Short |
| 整型 | int | Integer |
| 长整型 | long | Long |
| 单精度浮点型 | float | Float |
| 双精度浮点型 | double | Double |
| 字符型 | char | Character |
| 布尔型 | boolean | Boolean |


    1. // 1.int--->Integer a.自动装箱; b.使用Integer.valueOf(int i);方法装箱; c.使用构造方法
	2.	int i1 = 10;
	3.	Integer i2 = 10;// 自动装箱,当int的范围在-128~127之间的时候会在对象池中分配空间
	4.	Integer i3 = 10;// i2和i3这两个引用同时指向常量池中的一个int类型的值
	5.	Integer i4 = Integer.valueOf(i1);// 将一个int类型的值,装箱成Integer类型
	6.	Integer i5 = new Integer(i1);
	7.	// 测试,i5的转换,创建了新的对象,所以和其他比较为false
	8.	System.out.println(i1 == i2);// true
	9.	System.out.println(i1 == i3);// true
	10.	System.out.println(i2 == i3);// true
	11.	System.out.println(i3 == i4);// true
	12.	System.out.println(i4 == i5);// false
	13.	/*--------华丽的分割线--------*/
	14.	
	15.	// 2.Integer--->int a.自动拆箱; b.使用intValue();方法来进行拆箱;
	16.	Integer j1 = new Integer(15);// 创建的一个Integer
	17.	int j2 = j1;// 自动拆箱
	18.	int j3 = j1.intValue();// 用Integer类型的引用来调用Integer类中提供的方法,进行拆箱
	19.	// 测试
	20.	System.out.println(j1 == j2);// true
	21.	System.out.println(j1 == j3);// true
	22.	System.out.println(j2 == j3);// true
	23.	/*--------华丽的分割线--------*/
	24.	
	25.	// 3.int--->String a.可以使用字符串连接 b.可以使用String里面的valueOf方法 
	26.	int z1 = 18;
	27.	String z2 = z1 + "";// 任何一种数值类型和字符串进行运算,结果都是字符串类型.
	28.	// String 类型里面的valueOf方法可以返回任何类型的字符串表达形式
	29.	String z3 = String.valueOf(z1);// 同样,将一个数值类型转换成字符串类型,可以调用valueOf方法
	30.	String z4 = Integer.toString(z1);// 用Integer里面的toString()方法也可以转换
	31.	System.out.println(z3);
	32.	System.out.println(z4);
	33.	/*--------华丽的分割线--------*/
	34.	
	35.	// 4.String--->int只有有效的数值格式的String类型才可以被转换成一个int类型
	36.	String c1 = "123";
	37.	int c2 = Integer.parseInt(c1);// parse解析这个字符串,转换成int
	38.	System.out.println(c2);
	39.	/*--------华丽的分割线--------*/
	40.	
	41.	// 5.Integer--->String
	42.	Integer v1 = 180;// 自动装箱
	43.	String v2 = String.valueOf(v1);// String类型里面提供的valueOf很强大!!!!
	44.	String v3 = v1.toString();// Integr里面提供的toString方法也可以转换成字符串
	45.	System.out.println(v2);
	46.	System.out.println(v3);
	47.	System.out.println(v2 == v3);// false
	48.	/*--------华丽的分割线--------*/
	49.	
	50.	// 6.String--->Integer	a.使用pwrseInt解析	b.使用构造方法	c.使用Integer.valueOf(String str);进行转换
	51.	String b1 = "7896";
	52.	Integer b2 = Integer.parseInt(b1);
	53.	Integer b3 = new Integer(b1);
	54.	Integer b4 = Integer.valueOf(b1);
	55.	System.out.println(b2);
	56.	System.out.println(b3);
	57.	System.out.println(b4);


> 以上这些内容均可在JAVA的API帮助文档中找到