# 类与对象

## 1.类和对象的区别和联系

*   说明

    > 1. 类是抽象的，概念的，代表一类事物,比如人类,猫类.., 即它是数据类型.
    > 2. 对象是具体的，实际的，代表一个具体事物, 即 是实例.
    > 3. 类是对象的模板，对象是类的一个个体，对应一个实例


*   对象在内存中存在形式

    <figure><img src="../../../../.gitbook/assets/image (1) (1) (1).png" alt="" width="563"><figcaption></figcaption></figure>

## 2.属性/成员变量/字段

[goto：Object02.java](https://gitee.com/jia-yan\_dong/code/blob/master/Java/javacode/chapter07/Object02.java)

*   基本介绍

    > 1. 从概念或叫法上看： 成员变量 = 属性 = field(字段) （即 成员变量是用来表示属性的，授课中，统一叫 属性）
    > 2. 属性是类的一个组成部分，一般是基本数据类型,也可是引用类型(对象，数组)。比如我们前面定义猫类 的 int age 就 是属性


*   注意事项和细节说明

    > 1. 属性的定义语法同变量，示例：访问修饰符 属性类型 属性名; 这里老师简单的介绍访问修饰符： 控制属性的访问范围 有四种访问修饰符 public, proctected, 默认, private ,后面我会详细介绍
    > 2. 属性的定义类型可以为任意类型，包含基本类型或引用类型
    > 3. 属性如果不赋值，有默认值，规则和数组一致。具体说: int 0，short 0, byte 0, long 0, float 0.0,double 0.0，char \u0000， boolean false，String null

## 3.类和对象的内存分配机制

*   Java 内存的结构分析

    > 1. 栈： 一般存放基本数据类型(局部变量)
    > 2. 堆： 存放对象(Cat cat , 数组等)
    > 3. 方法区：常量池(常量，比如字符串)， 类加载信息
    > 4.
    >
    >     <figure><img src="../../../../.gitbook/assets/image (3).png" alt="" width="563"><figcaption></figcaption></figure>


* Java 创建对象的流程简单分析
  * {% code lineNumbers="true" %}
    ```java
    Person p = new Person();
    p.name = “jack”;
    p.age = 10
    ```
    {% endcode %}
  * > 1. 先加载 Person 类信息(属性和方法信息, 只会加载一次)
    > 2. 在堆中分配空间, 进行默认初始化(看规则)
    > 3. 把地址赋给 p , p 就指向对象
    > 4. 进行指定初始化， 比如 p.name =”jack” p.age = 10
