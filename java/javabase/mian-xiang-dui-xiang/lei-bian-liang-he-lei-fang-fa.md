# 类变量和类方法

## 1.类变量

*   什么是类变量

    [goto：ChildGame.java](https://gitee.com/jia-yan\_dong/code/blob/master/Java/javacode/chapter10/src/com/hspedu/static\_/ChildGame.java)

    > 类变量也叫静态变量/静态属性，是该类的所有对象共享的变量，任何一个该类的对象去访问它时，取到的都是相同的值，同样任何一个该类的对象去修改它时修改的也是同一个变量


*   类变量内存布局

    > 1. 有些书说在方法区，和<mark style="color:yellow;">**jdk版本**</mark>有关系，记住一点：static变量是对象共享不管static变量在哪里
    > 2. 共识
    >    1. static变量是同一个类所有对象共享
    >    2. static类变量，在类加载的时候就生成了
    > 3. 相关文章
    >    1. [https://blog.csdn.net/x\_iya/article/details/81260154/](https://blog.csdn.net/x\_iya/article/details/81260154/)
    >    2. [https://www.zhihu.com/question/59174759/answer/163207831](https://www.zhihu.com/question/59174759/answer/163207831)


*   注意事项和使用细节

    [goto：StaticDetail.java](https://gitee.com/jia-yan\_dong/code/blob/master/Java/javacode/chapter10/src/com/hspedu/static\_/StaticDetail.java)

    > 1. 什么时候需要用类变量当我们需要让某个类的所有对象都共享一个变量时，就可以考虑使用类变量（静态变量)：比如：定义学生类，统计所有学生共交多少钱。
    > 2. 类变量与实例变量（普通属性）区别类变量是该类的所有对象共享的，而实例变量是每个对象独享的
    > 3. 加上static称为类变量或静态变量，否则称为实例变量/普通变量/非静态变量&#x20;
    > 4. 类变量可以通过类名.类变量名或者对象名.类变量名来访问，但java设计者推荐我们使用类名类变量名方式访问。【**前提是满足访问修饰符的访问权限和范围**】&#x20;
    > 5. 实例变量不能通过 类名.类变量名 方式访问&#x20;
    > 6. 类变量是在类加载时就初始化了，也就是说，即使你没有创建对像，只要类加载了，就可以使用类变量了。
    > 7. 类变量的生命周期是随类的加载开始，随着类消亡而销毁。

## 2.类方法

*   基本介绍

    [goto：StaticMethod.java](https://gitee.com/jia-yan\_dong/code/blob/master/Java/javacode/chapter10/src/com/hspedu/static\_/StaticMethod.java)

    > 类方法也叫静态方法


*   类方法经典的使用场景

    > 1. 当方法中不涉及到任何和对象相关的成员，则可以将方法设计成静态方法提高开发效率。比如：工具类中的方法utils Math类、Arrays类、Collections集合类
    > 2. 在实际开发，往往会将一些通用的方法，设计成静态方法，这样我们不需要创建对象就可以使用了，比如打印一维数组，冒泡排序，完成某个计算任务等


*   注意事项和使用细节

    [goto：StaticMethodDetail.java](https://gitee.com/jia-yan\_dong/code/blob/master/Java/javacode/chapter10/src/com/hspedu/static\_/StaticMethodDetail.java)

    > 1. 类方法和普通方法都是随看类的加载而加载，将结构信息存储在方法区：类方法中无this的参数普通方法中隐含着this的参数&#x20;
    > 2. 类方法可以通过类名调用，也可以通过对象名调用。
    > 3. 普通方法和对象有关，需要通过对象名调用，比如对象名.方法名（参数），不能通过类名调用。
    > 4. 类方法中不允许使用和对象有关的关键字，比如this和super。.普通方法（成员方法）可以。
    > 5. 类方法（静态方法）中只能访问静态变量或静态方法。
    > 6. 普通成损方法，既可以访问非静态成员，也可以访问静态成员。
