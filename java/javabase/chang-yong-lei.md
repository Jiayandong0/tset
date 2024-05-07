# 常用类

[goto：chapter13](https://gitee.com/jia-yan\_dong/code/tree/master/Java/javacode/chapter13)

## 1.包装类

*   包装类的分类



    |  基本数据类型 |    包装类    |
    | :-----: | :-------: |
    | boolean |  Boolean  |
    |   char  | Character |
    |   byte  |    Byte   |
    |  short  |   Short   |
    |   int   |  Integer  |
    |   long  |    Long   |
    |  float  |   Float   |
    |  double |   Double  |
*   包装类和基本数据的转换

    [goto：Integer01.java](https://gitee.com/jia-yan\_dong/code/blob/master/Java/javacode/chapter13/src/com/hspedu/wrapper/Integer01.java)

    > 1. jdk5前的手动装箱和拆箱方式，装箱：基本类型->包装类型，反之，拆箱&#x20;
    > 2. jdk5以后（含jdk5)的自动装箱和拆箱方式
    > 3. 自动装箱底层调用的是valueOf方法，比如Integer..valueOf()


*   Integer 类和 Character 类的常用方法

    [goto：WrapperMethod.java](https://gitee.com/jia-yan\_dong/code/blob/master/Java/javacode/chapter13/src/com/hspedu/wrapper/WrapperMethod.java)
*   Intege 类面试题总结

    [goto：WrapperExercise03.java](https://gitee.com/jia-yan\_dong/code/blob/master/Java/javacode/chapter13/src/com/hspedu/wrapper/WrapperExercise03.java)

## 2.String类

*   String 类的理解和创建对象

    [goto：String01.java](https://gitee.com/jia-yan\_dong/code/blob/master/Java/javacode/chapter13/src/com/hspedu/string\_/String01.java)

    > 1. String对象用于保存字符串，也就是一组字符序列
    > 2. 字符串常量对象是用双引号括起的字符序列。例如："你好”、"12.97"、"boy“"等
    > 3. 字符串的字符使用Unicode字符编码，一个字符（不区分字母还是汉字）占两个字节。


*   两种创建 String 对象的区别

    > 1. 方式一：String s = "hello";
    >    1. 先从常量池查看是否有"hello”数据空间，如果有，直接指向；如果没有则重新创建，然后指向。S最终指向的是常量池的空间地址
    > 2. 方式二：String s = new String("hello");
    >    1. 先在堆中创建空间，里面维护了value属性，指向常量池的hello空间。如果常量池没有"hello”,重新创建，如果有，直接通过value指向。最终指向的是堆中的空间地址
    > 3.  两种方式的内存分布图
    >
    >
    >
    >     <figure><img src="../../.gitbook/assets/image.png" alt="" width="375"><figcaption></figcaption></figure>


*   String测试题

    > 1. [goto：StringExercise01.java](https://gitee.com/jia-yan\_dong/code/blob/master/Java/javacode/chapter13/src/com/hspedu/string\_/StringExercise01.java)
    > 2. [goto：StringExercise02.java](https://gitee.com/jia-yan\_dong/code/blob/master/Java/javacode/chapter13/src/com/hspedu/string\_/StringExercise02.java)
    > 3. [goto：StringExercise03.java](https://gitee.com/jia-yan\_dong/code/blob/master/Java/javacode/chapter13/src/com/hspedu/string\_/StringExercise03.java)
    > 4. [goto：StringExercise04.java](https://gitee.com/jia-yan\_dong/code/blob/master/Java/javacode/chapter13/src/com/hspedu/string\_/StringExercise04.java)
    > 5. [goto：StringExercise05.java](https://gitee.com/jia-yan\_dong/code/blob/master/Java/javacode/chapter13/src/com/hspedu/string\_/StringExercise05.java)


*   字符串的特性

    > 1. String是一个final类，代表不可变的字符序列
    > 2. 字符串是不可变的。一个字符串对象一旦被分配，其内容是不可变的


*   面试题

    > 1. [goto：StringExercise06.java](https://gitee.com/jia-yan\_dong/code/blob/master/Java/javacode/chapter13/src/com/hspedu/string\_/StringExercise06.java)
    > 2. [goto：StringExercise07.java](https://gitee.com/jia-yan\_dong/code/blob/master/Java/javacode/chapter13/src/com/hspedu/string\_/StringExercise07.java)
    > 3. [goto：StringExercise08.java](https://gitee.com/jia-yan\_dong/code/blob/master/Java/javacode/chapter13/src/com/hspedu/string\_/StringExercise08.java)
    > 4. [goto：StringExercise09.java](https://gitee.com/jia-yan\_dong/code/blob/master/Java/javacode/chapter13/src/com/hspedu/string\_/StringExercise09.java)
    > 5. [goto：StringExercise10.java](https://gitee.com/jia-yan\_dong/code/blob/master/Java/javacode/chapter13/src/com/hspedu/string\_/StringExercise10.java)


*   String 类的常见方法

    goto：[StringMethod01.java](https://gitee.com/jia-yan\_dong/code/blob/master/Java/javacode/chapter13/src/com/hspedu/string\_/StringMethod01.java) [StringMethod02.java](https://gitee.com/jia-yan\_dong/code/blob/master/Java/javacode/chapter13/src/com/hspedu/string\_/StringMethod02.java)

    > String类是保存字符串常量的。每次更新都需要重新开辟空间，效率较低，因此java设计者还提供了String Builder和StringBuffer来增强String的功能，并提高效率。

## 3.StringBuffer 和 StringBuilder

*   基本介绍

    goto：.java

    > 1.


*

    goto：.java

    > 1.


*   注意事项和使用细节

    goto：.java

    > 1. 1

## 4.Math类

*   基本介绍

    goto：.java

    > 1.


*

    goto：.java

    > 1.


*   注意事项和使用细节

    goto：.java

    > 1. 1

## 5.Arrays类

*   基本介绍

    goto：.java

    > 1.


*

    goto：.java

    > 1.


*   注意事项和使用细节

    goto：.java

    > 1. 1

## 6.System类

*   基本介绍

    goto：.java

    > 1.


*

    goto：.java

    > 1.


*   注意事项和使用细节

    goto：.java

    > 1. 1

## 7.BigInteger 和 BigDecimal

*   基本介绍

    goto：.java

    > 1.


*

    goto：.java

    > 1.


*   注意事项和使用细节

    goto：.java

    > 1. 1

## 8.日期类

*   基本介绍

    goto：.java

    > 1.


*

    goto：.java

    > 1.


*   注意事项和使用细节

    goto：.java

    > 1. 1
