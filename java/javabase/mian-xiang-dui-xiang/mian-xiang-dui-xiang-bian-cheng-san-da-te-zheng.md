# 面向对象编程三大特征

*   基本介绍

    [goto：Encapsulation01.java](https://gitee.com/jia-yan\_dong/code/blob/master/Java/javacode/chapter08/src/com/hspedu/encap/Encapsulation01.java)

    > 封装(encapsulation)就是把抽象出的数据\[属性]和对数据的操作\[方法]封装在一起，数据被保护在内部，程序的其它部分只有通过被授权的操作\[方法]，才能对数据进行操作。


*   封装的实现步骤 (三步)

    > 1. 1\)将属性进行私有化private,（不能直接修改属性)&#x20;
    > 2. 提供一个公共的(public)set方法，用于对属性判断并赋值
    > 3. 提供一个公共的(public)get方法，用于获取属性的值&#x20;

## 2.继承

*   基本介绍

    [goto：Extends01.java](https://gitee.com/jia-yan\_dong/code/blob/master/Java/javacode/chapter08/src/com/hspedu/extend\_/Extends01.java)

    > 继承可以解决代码复用,让我们的编程更加靠近人类思维.当多个类存在相同的属性(变量)和方法时,可以从这些类中 抽象出父类,在父类中定义这些相同的属性和方法，所有的子类不需要重新定义这些属性和方法，只需要通过 extends 来 声明继承父类即可
*   注意事项和使用细节

    [goto：ExtendsDetail.java](https://gitee.com/jia-yan\_dong/code/blob/master/Java/javacode/chapter08/src/com/hspedu/extend\_/ExtendsDetail.java)

    > 1. 子类继承了所有的属性和方法，非私有的属性和方法可以在子类直接访问, 但是私有属性和方法不能在子类直接访 问，要通过父类提供公共的方法去访问
    > 2. 子类必须调用父类的构造器， 完成父类的初始化
    > 3. 当创建子类对象时，不管使用子类的哪个构造器，默认情况下总会去调用父类的无参构造器，如果父类没有提供无 参构造器，则必须在子类的构造器中用 super 去指定使用父类的哪个构造器完成对父类的初始化工作，否则，编译不会通过
    > 4. 如果希望指定去调用父类的某个构造器，则显式的调用一下 : super(参数列表)
    > 5. super 在使用时，必须放在构造器第一行(super 只能在构造器中使用)
    > 6. super() 和 this() 都只能放在构造器第一行，因此这两个方法不能共存在一个构造器
    > 7. java 所有类都是 Object 类的子类, Object 是所有类的基类.
    > 8. 父类构造器的调用不限于直接父类！将一直往上追溯直到 Object 类(顶级父类)
    > 9. 子类最多只能继承一个父类(指直接继承)，即 java 中是单继承机制。
    > 10. 不能滥用继承，子类和父类之间必须满足 is-a 的逻辑关系


*   继承的<mark style="color:yellow;">**本质**</mark>分析

    [goto：ExtendsTheory.java](https://gitee.com/jia-yan\_dong/code/blob/master/Java/javacode/chapter08/src/com/hspedu/extend\_/ExtendsTheory.java)

    > * 我们看一个案例来分析当子类继承父类，创建子类对象时，内存中到底发生了什么？
    > * 当子类对象创建好后，<mark style="color:yellow;">建立查找的关系</mark>
    > *   子类创建的内存布局
    >
    >     <figure><img src="../../../.gitbook/assets/image (7).png" alt=""><figcaption></figcaption></figure>
*   super 关键字

    *   基本介绍

        [goto：super](https://gitee.com/jia-yan\_dong/code/blob/master/Java/javacode/chapter08/src/com/hspedu/extend\_/super\_/)

        > super 代表**父类的引用**，**用于访问父类的属性**、**方法**、**构造器**



    *   注意事项和使用细节

        > 1. 调用父类的构造器的好处（分工明确，父类属性由父类初始化，子类的属性由子类初始化)
        > 2. 当子类中有和父类中的成损（属性和方法）重名时，为了访问父类的成员，必须通过super。.如果没有重名，使用super、.this、直接访问是一样的效果
        > 3. superl的访问不限于直接父类，如果爷爷类和本类中有同名的成员，也可以使用 super去访问爷爷类的成员；如果多个基类（上级类）中都有同名的成员，使用super访问遵循就近原则。A->B->C,当然也需要遵守访问权限的相关规则


    *   super 和 this 的比较



        <table><thead><tr><th width="88" align="center">No</th><th width="130" align="center">区别点</th><th align="center">this</th><th align="center">super</th></tr></thead><tbody><tr><td align="center">1</td><td align="center">访问属性</td><td align="center">访问本类中的属性，如果本类没有此属性则从父类中继续查找</td><td align="center">从父类开始查找属性</td></tr><tr><td align="center">2</td><td align="center">调用方法</td><td align="center">访问本类中的方法如果本类没有此方法则从父类继续查找</td><td align="center">从父类开始查找方法</td></tr><tr><td align="center">3</td><td align="center">调用构造器</td><td align="center">调用本类构造器，必须放在构造器的首行</td><td align="center">调用父类构造器，必须放在子类构造器的首行</td></tr><tr><td align="center">4</td><td align="center">特殊</td><td align="center">表示当前对象</td><td align="center">子类中访问父类对象</td></tr></tbody></table>
    *   方法重写/覆盖(override)

        *   基本介绍

            [goto：Dog.java](https://gitee.com/jia-yan\_dong/code/blob/master/Java/javacode/chapter08/src/com/hspedu/extend\_/override\_/Dog.java)

            > 简单的说：方法覆盖（重写）就是子类有一个方法，和父类的某个方法的名称、返回类型、参数一样，那么我们就说子类的这个方法覆盖了父类的方法



        *   注意事项和使用细节

            > 1. 子类的方法的形参列表方法名称，要和父类方法的形参列表，方法名称完全一样
            > 2. 子类方法的返回类型和父类方法返回类型一样，或者是父类返回类型的子类比如父类返回类型是Object,子类方法返回类型是String
            > 3. 子类方法不能缩小父类方法的访问权限

## 3.多态

*   基本介绍

    [goto：.java](mian-xiang-dui-xiang-bian-cheng-san-da-te-zheng.md#id-1.-cheng-yuan-fang-fa)

    > 1.


*   xx

    > 1. 1


*   注意事项和使用细节

    [goto：.java](mian-xiang-dui-xiang-bian-cheng-san-da-te-zheng.md#id-6.-zuo-yong-yu)

    > 1. 1
