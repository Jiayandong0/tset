# Java

## 1.Java诞生的小故事

* **Java官网：**[**https://www.java.com/zh-CN/**](https://www.java.com/zh-CN/)
*   Java API文档

    > * API (Application Programming Interface,应用程序编程接口)是Java提供的基本编程接口(java提供的类还有相关的方法)。
    > * Java语言提供了大量的基础类，因此Oracle公司也为这些基础类提供了相应的API文档，用于告诉开发者如何使用这些类，以及这些类里包含的方法。

    > ***
    >
    > * 中文在线文档： [https://www.matools.com/api/java11](https://www.matools.com/api/java11)

> * 1990sun公司启动绿色计划
> * 1992创建oak(橡树)语言->java
> * 1994 gosling参加硅谷大会演示java功能，震惊世界
> * 1995sun正式发布java第1个版本
> * 2009年，甲骨文公司宣布收购Sun
> * 2011,发布java7
> *   其它java版本发布详情&#x20;
>
>     [https://www.oracle.com/java/technologies/java-se-support-roadmap.html](https://www.oracle.com/java/technologies/java-se-support-roadmap.html)

*   Java之父

    > * **Java之父是詹姆斯·高斯林(James Gosling)**
    >
    > <img src=".gitbook/assets/image (1) (1).png" alt="" data-size="original">

## 2.Java 技术体系平台

> *   Java SE(Java Standard Edition) <mark style="color:yellow;">**标准版**</mark>
>
>     支持面向桌面级应用（如Windows下的应用程序）的Java平台，提供了完整的Java核心 API，此版本以前称为J2SE&#x20;
> *   Java EE(Java Enterprise Edition) <mark style="color:yellow;">**企业版**</mark>
>
>     是为开发企业环境下的应用程序提供的一套解决方案。该技术体系中包含的技术如：Servlet、Jsp等，主要针对于Web应用程序开发。版本以前称为J2EE&#x20;
> *   Java ME(Java Micro Edition) <mark style="color:yellow;">**小型版**</mark>
>
>     支持Java程序运行在移动终端（手机、PDA),上的平台，对Java API有所精简，并加入了针对移动终端的支特，此版本以前称为J2ME

## 3.Java重要特点

> 1. Java 语言是面向对象的(<mark style="color:yellow;">**OOP**</mark>)
> 2. Java 语言是<mark style="color:yellow;">**健壮的**</mark>。Java 的强类型机制、异常处理、垃圾的自动收集等是 Java 程序健壮性的重要保证
> 3.  Java 语言是<mark style="color:yellow;">**跨平台性的**</mark>。\[即: 一个编译好的.class 文件可以在多个系统下运行，这种特性称为跨平台]
>
>
>
>     <figure><img src=".gitbook/assets/image (1) (1) (1) (1).png" alt="" width="375"><figcaption></figcaption></figure>
> 4. Java 语言是解释型的\[了解]&#x20;
>    * 解释性语言：javascript,PHP, java&#x20;
>    * 编译性语言: c / c++&#x20;
>    * 区别是：解释性语言，编译后的代码，不能直接被机器执行,需要解释器来执行, 编译性语言, 编译后的代码, 可 以直接被机器执行, c /c++

## 4.下载安装JDK

* 官网地址：[https://www.oracle.com/java/technologies/downloads/](https://www.oracle.com/java/technologies/downloads/)
*   细节说明

    > * 安装路径不要有中文或者特殊符号如空格等。
    > * 比如d:\program\jdk8
    > * 当提示安装JRE时，可以选择不安装，也可以安装


*   Java配置环境变量path

    > 1. 我的电脑-属性-高级系统设置-环境变量&#x20;
    > 2. 增加JAVA HOME环境变量，指向jdk的安装目录d:\program\jdk8
    > 3. 编辑path环境变量，增加%JAVA\_HOME%\bin
    > 4. 打开DOS命令行，任意目录下敲入javac/java。如果出现javac的参数信息，配置成功。
