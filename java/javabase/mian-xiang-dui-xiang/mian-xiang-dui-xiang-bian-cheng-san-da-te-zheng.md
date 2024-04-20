# 面向对象编程三大特征

## 1.封装

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

### 1.多态的介绍

*   基本介绍

    [goto：PloyMethod.java](https://gitee.com/jia-yan\_dong/code/blob/master/Java/javacode/chapter08/src/com/hspedu/poly\_/PolyMethod.java)

    > 方法或对象具有多种形态。是面向对象的第三大特征，多态是建立在封装和继承基础之上的


*   对象的多态

    [goto：PloyObject.java](https://gitee.com/jia-yan\_dong/code/blob/master/Java/javacode/chapter08/src/com/hspedu/poly\_/objectpoly\_/PolyObject.java)

    > 1. 一个对象的编译类型和运行类型可以不一致
    > 2. 编译类型在定义对象时，就确定了，不能改变
    > 3. 运行类型是可以变化的
    > 4. 编译类型看定义时=号的左边，运行类型看=号的右边


*   注意事项和使用细节

    [goto：PolyDetail.java](https://gitee.com/jia-yan\_dong/code/blob/master/Java/javacode/chapter08/src/com/hspedu/poly\_/detail\_/PolyDetail.java)

    > 1. 多态的前提是：两个对象（类）存在继承关系多态的向上转型
    > 2. 多态的向上转型
    >    1. 本质：父类的引用指向了子类的对象
    >    2. 语法：父类类型  引用名 = new 子类类型();
    >    3. 特点：编译类型看左边，运行类型看右边。可以调用父类中的所有成员（需遵守访问权限），不能调用子类中特有成员;最终运行效果看子类的具体实现！
    > 3. 多态向下转型
    >    1. 语法：子类类型 引用名=（子类类型）父类引用;
    >    2. 只能强转父类的引用，不能强转父类的对象
    >    3. 要求父类的引用必须指向的是当前目标类型的对象
    >    4. 当向下转型后，可以调用子类类型中所有的成员
    > 4. 属性没有重写之说！属性的值看编译类型 [goto：PolyDetail02.java](https://gitee.com/jia-yan\_dong/code/blob/master/Java/javacode/chapter08/src/com/hspedu/poly\_/detail\_/PolyDetail02.java)
    > 5. instanceOf 比较操作符，用于判断对象的运行类型是否为 XX 类型或 XX 类型的子类型 [goto：PolyDetail03.java](https://gitee.com/jia-yan\_dong/code/blob/master/Java/javacode/chapter08/src/com/hspedu/poly\_/detail\_/PolyDetail03.java)


*   多态的应用

    [goto：PloyArray.java](https://gitee.com/jia-yan\_dong/code/blob/master/Java/javacode/chapter08/src/com/hspedu/poly\_/polyar\_/PloyArray.java)

    > 1. 数组的定义类型为父类类型，里面保存的实际元素类型为子类类型&#x20;
    > 2. 应用实例:现有一个继承结构如下：要求创建 1 个 Person 对象、2 个 Student 对象和 2 个 Teacher 对象, 统一放在数组 中，并调用每个对象

### 2.java 的动态绑定机制

*   基本介绍

    [goto：DynamicBinding.java](https://gitee.com/jia-yan\_dong/code/blob/master/Java/javacode/chapter08/src/com/hspedu/poly\_/dynamic\_/DynamicBinding.java)

    > 1. 当调用对象方法的时候，<mark style="color:yellow;">该方法会和该对象的内存地址/运行类型绑定</mark>
    > 2. 当调用对象属性时，<mark style="color:yellow;">没有动态绑定机制</mark>，哪里声明，那里使用
