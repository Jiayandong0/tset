# 接口

[goto：interface\_](https://gitee.com/jia-yan\_dong/code/tree/master/Java/javacode/chapter10/src/com/hspedu/interface\_)

*   基本介绍

    [goto：Interface01.java](https://gitee.com/jia-yan\_dong/code/blob/master/Java/javacode/chapter10/src/com/hspedu/interface\_/Interface01.java)

    > 1. 接口就是给出一些没有实现的方法，封装到一起，到某个类要使用的时候，在根据具体情况把这些方法写出来
    > 2. 接口是更加抽象的抽象的类，抽象类里的方法可以有方法体，接口里的所有方法都没有方法体【jdk7.0】。接口体现了程序设计的多态和高内聚低偶合的设计思想特
    > 3. 别说明：Jdk8.0后接口类可以有静态方法，默认方法，也就是说接口中可以有方法的具体实现


*   注意事项和使用细节

    goto：[InterfaceDetail01.java](https://gitee.com/jia-yan\_dong/code/blob/master/Java/javacode/chapter10/src/com/hspedu/interface\_/InterfaceDetail01.java) [InterfaceDetail02.java](https://gitee.com/jia-yan\_dong/code/blob/master/Java/javacode/chapter10/src/com/hspedu/interface\_/InterfaceDetail02.java)

    > 1. 接口不能被实例化
    > 2. 接口中所有的方法是public方法，接口中抽象方法，可以不用abstract修饰
    > 3. 一个普通类实现接口就必须将该接口的所有方法都实现
    > 4. 抽象类实现接口，可以不用实现接口的方法
    > 5. 一个类同时可以实现多个接口
    > 6. 接口中的属性，只能是final的，而且是public static final修饰符&#x20;
    > 7. 接口中属性的访问形式：接口名.属性名
    > 8. 接口不能继承其它的类，但是可以继承多个别的接口
    > 9. 接口的修饰符只能是public和默认，这点和类的修饰符是一样的


*   实现接口 vs 继承类

    [goto：ExtendsVsInterface.java](https://gitee.com/jia-yan\_dong/code/blob/master/Java/javacode/chapter10/src/com/hspedu/interface\_/ExtendsVsInterface.java)

    > 1. 接口和继承解决的问题不同
    >    1. 继承的价值主要在于：解决代码的<mark style="color:yellow;">**复用性和可维护性**</mark>
    >    2. 接口的价值主要在于：设计，设计好各种规范（方法），让其它类去实现这些方法。即更加的灵活
    > 2. 接口比继承更加灵活接口比继承更加灵活，继承是满足is\~a的关系，而接口只需满足like - a的关系
    > 3. 接口在一定程度上实现代码解耦\[即：接口规范性+动态绑定机制]


*   接口的多态特性

    > 1. 多态参数 [goto：InterfacePolyParameter.java](https://gitee.com/jia-yan\_dong/code/blob/master/Java/javacode/chapter10/src/com/hspedu/interface\_/InterfacePolyParameter.java)
    > 2. 多态数组[ goto：InterfacePolyArr.java](https://gitee.com/jia-yan\_dong/code/blob/master/Java/javacode/chapter10/src/com/hspedu/interface\_/InterfacePolyArr.java)
    > 3. 接口存在<mark style="color:yellow;">**多态传递**</mark>现象[ goto：InterfacePolyPass.java](https://gitee.com/jia-yan\_dong/code/blob/master/Java/javacode/chapter10/src/com/hspedu/interface\_/InterfacePolyPass.java)

