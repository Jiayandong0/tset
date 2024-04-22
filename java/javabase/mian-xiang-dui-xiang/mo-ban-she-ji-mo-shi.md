# 模板设计模式

*   基本介绍

    > 抽象类体现的就是一种模板模式的设计，抽象类作为多个子类的通用模板，子类在抽象类的基础上进行扩展、改造，但子类总体上会保留抽象类的行为方式


*   模板设计模式能解决的问题

    goto：.java

    > 1. 当功能内部一部分实现是确定，一部分实现是不确定的。这时可以把不确定的部分暴露出去，让子类去实现
    > 2. 编写一个抽象父类，父类提供了多个子类的通用方法，并把一个或多个方法留给其子类实现，就是一种模板模式。


*   最佳实践

    [goto：TestTemplate.java](https://gitee.com/jia-yan\_dong/code/blob/master/Java/javacode/chapter10/src/com/hspedu/abstract\_/TestTemplate.java)

    > 1. 需求
    >    1. 有多个类，完成不同的任务job
    >    2. 要求统计得到各自完成任务的时间
