# 代码块

[goto：codeblock\_](https://gitee.com/jia-yan\_dong/code/tree/master/Java/javacode/chapter10/src/com/hspedu/codeblock\_)

*   基本介绍

    > 1. 代码化块又称为<mark style="color:yellow;">**初始化块**</mark>，属于类中的成员\[即是类的一部分]，类似于方法，将逻辑语句封装在方法体中，通过包围起来。
    > 2. 但和方法不同，没有方法名，没有返回，没有参数，只有方法体，而且不用通过对象或类显式调用，而是加载类时，或创建对象时隐式调用。


*   基本语法

    {% code lineNumbers="true" %}
    ```java
    修饰符 {
        代码
    }
    ```
    {% endcode %}

    > 1. 修饰符可选，要写的话，也只能写static
    > 2. 代码块分为两类，使用static修饰的叫静态代码块，没有static修饰的，叫普通代码块/非静态代码块
    > 3. 逻辑语句可以为任何逻辑语句（输入、输出、方法调用、循环、判断等
    > 4. ;号可以写上，也可以省略。


*   代码块的好处

    [goto：CodeBlock01.java](https://gitee.com/jia-yan\_dong/code/blob/master/Java/javacode/chapter10/src/com/hspedu/codeblock\_/CodeBlock.java)

    > 1. 相当于另外一种形式的构造器（对构造器的补充机制），可以做初始化的操作&#x20;
    > 2. 场景：如果多个构造器中都有重复的语句，可以抽取到初始化块中，提高代码的重用性


*   注意事项和细节讨论

    [goto：CodeBlockDetail01.java](https://gitee.com/jia-yan\_dong/code/blob/master/Java/javacode/chapter10/src/com/hspedu/codeblock\_/CodeBlockDetail01.java)

    > 1. static代码快也叫静态代码块，作用就是对类进行初始化，而且它随着<mark style="color:yellow;">**类的加载**</mark>而执行，并且<mark style="color:yellow;">**只会执行一次**</mark>。如果是普通代码块，每创建一个对象，就执行。
    > 2. 类什么时候被加载
    >    1. 创建对象实例时(new)
    >    2. 创建子类对象实例，父类也会被加载
    >    3. 使用类的静态成员时（静态属性，静态方法）
    > 3. 普通的代码块，在创建对象实例时，：会被隐式的调用。被创建一次，就会调用一次。如果只是使用类的静态成员时，普通代码块并不会执行
    > 4.  创建一个对象时，在一个类调用顺序是:
    >
    >     [goto：CodeBlockDetail02.java](https://gitee.com/jia-yan\_dong/code/blob/master/Java/javacode/chapter10/src/com/hspedu/codeblock\_/CodeBlockDetail02.java)
    >
    >     1. 调用静态代码块和静态属性初始化（注意：静态代码块和静态属性初始化调用的优先级一样，如果有多个静态代码块和多个静态变量初始化，则按他们定义的顺序调用)
    >     2. 调用普通代码块和普通属性的初始化（注意：普通代码块和普通属性初始化调用的优先级一样，如果有多个普通代码块和多个普通属性初始化，则按定义顺序调用)
    >     3. 调用构造方法。
    > 5.  构造器的最前面其实隐含了super()和调用普通代码块，新写一个类演示静态相关的代码块，属性初始化，在类加载时，就执行完毕,因此是优先于构造器和普通代码块执行的
    >
    >     [goto：CodeBlockDetail03.java](https://gitee.com/jia-yan\_dong/code/blob/master/Java/javacode/chapter10/src/com/hspedu/codeblock\_/CodeBlockDetail03.java)
    > 6.  <mark style="color:yellow;">**我们看一下创建一个子类对象时（继承关系），他们的静态代码块，静态属性初始化，普通代码块，普通属性初始化，构造方法的调用顺序如下：**</mark>
    >
    >     [goto：CodeBlockDetail04.java](https://gitee.com/jia-yan\_dong/code/blob/master/Java/javacode/chapter10/src/com/hspedu/codeblock\_/CodeBlockDetail04.java)
    >
    >     1. 父类的静态代码块和静态属性（优先级一样，按定义顺序执行）
    >        1. 子类的静态代码块和静态属性（优先级一样，按定义顺序执行）
    >        2. 父类的普通代码块和普通属性初始化（优先级一样，按定义顺序执行）
    >        3. 父类的构造方法
    >        4. 子类的普通代码块和普通属性初始化（优先级一样，按定义顺序执行)
    >        5. 子类的构造方法/面试题
    > 7. 静态代码块只能直接调用静态成员（静态属性和静态方法），普通代码块可以调用任意成员。
