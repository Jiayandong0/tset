# 抽象类

[goto：abstract\_](https://gitee.com/jia-yan\_dong/code/tree/master/Java/javacode/chapter10/src/com/hspedu/abstract\_)

*   基本介绍

    [goto：Abstract01.java](https://gitee.com/jia-yan\_dong/code/blob/master/Java/javacode/chapter10/src/com/hspedu/abstract\_/Abstract01.java)

    > 1. 用abstract关键字来修饰一个类时，这个类就叫抽象类&#x20;
    > 2. 用abstract关键字来修饰一个方法时，这个方法就是抽象方法
    > 3. 抽象类的价值更多作用是在于设计，是设计者设计好后，让子类继承并实现抽象类
    > 4. 抽象类，在框架和设计模式使用较多


*   注意事项和使用细节

    goto：[AbstractDetail01.java](https://gitee.com/jia-yan\_dong/code/blob/master/Java/javacode/chapter10/src/com/hspedu/abstract\_/AbstractDetail01.java) [AbstractDetail02.java](https://gitee.com/jia-yan\_dong/code/blob/master/Java/javacode/chapter10/src/com/hspedu/abstract\_/AbstractDetail01.java)

    > 1. 抽象类不能被实例化
    > 2. 抽象类不一定要包含abstract方法。也就是说，抽象类可以没有abstract方法
    > 3. 一旦类包含了abstract方法，则这个类必须声明为abstract
    > 4. abstract只能修饰类和方法，不能修饰属性和其它的
    > 5. 抽象类可以有任意成损【抽象类本质还是类】，比如：非抽象方法、构造器、静态属性等等&#x20;
    > 6. 抽象方法不能有主体，即不能实现
    > 7. 如果一个类继承了抽象类，则它必须实现抽象类的所有抽象方法，除非它自己也声明为abstract类
    > 8. 抽象方法不能使用private、final和static来修饰，因为这些关键字都是和重写相违背的。
