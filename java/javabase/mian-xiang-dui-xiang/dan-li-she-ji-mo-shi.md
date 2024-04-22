# 单例设计模式

*   基本介绍

    > 1. 所谓类的单例设计模式，就是采取一定的方法保证在整个的软件系统中，对某个类只能存在一个对象实例，并且该类只提供一个取得其对象实例的方法&#x20;
    > 2. 单例模式有两种方式：
    >    1. 饿汉式 [goto：SingleTon01.java](https://gitee.com/jia-yan\_dong/code/blob/master/Java/javacode/chapter10/src/com/hspedu/single\_/SingleTon01.java)
    >    2. 懒汉式 [goto：SingleTon02.java](https://gitee.com/jia-yan\_dong/code/blob/master/Java/javacode/chapter10/src/com/hspedu/single\_/SingleTon02.java)


*   单例模式的实现

    > 1. 构造器私有化 => 防止直接 new&#x20;
    > 2. 类的内部创建对象&#x20;
    > 3. 向外暴露，个静态的公共方法。 getInstance


*   饿汉式 VS 懒汉式

    > 1. 二者最主要的区别在于创建对象的<mark style="color:yellow;">**时机**</mark>不同：饿汉式是在类加载就创建了对象实例，而懒汉式是在使用时才创建。&#x20;
    > 2. 饿汉式不存在线程安全问题，懒汉式存在线程安全问题。（后面学习线程后，会完善一把)&#x20;
    > 3. 饿汉式存在浪费资源的可能。因为如果程序员一个对象实例都没有使用，那么饿汉式创建的对象就浪费了，懒汉式是使用时才创建，就不存在这个问题。&#x20;
    > 4. 在我们javaSE标准类中，java.lang.Runtime就是经典的单例模式。
