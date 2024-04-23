# 内部类

[goto：ineerclass](https://gitee.com/jia-yan\_dong/code/tree/master/Java/javacode/chapter10/src/com/hspedu/ineerclass)

## 1.局部内部类

*   基本介绍

    [goto：LocalInnerClass.java](https://gitee.com/jia-yan\_dong/code/blob/master/Java/javacode/chapter10/src/com/hspedu/ineerclass/LocalInnerClass.java)

    > 1. 说明：局部内部类是定义在外部类的局部位置，比如方法中，并且有类名。&#x20;
    > 2. 可以直接访问外部类的所有成损，包含私有的&#x20;
    > 3. 不能添加访问修饰符，因为它的地位就是一个局部变量。局部变量是不能使用修饰符的。但是可以使用final修饰，因为局部变量也可以使用final
    > 4. 作用域：仅仅在定义它的方法或代码块中
    > 5. 局部内部类--访问-->外部类的成员\[访问方式：直接访问]&#x20;
    > 6. 外部类--访问-->局部内部类的成员访问方式：创建对象，再访问（注意：必须在作用域内）
    > 7. 作用域在方法体或者代码块中，本质仍然是一个类&#x20;
    > 8. 外部其他类--不能访问-->局部内部类（因为局部内部类地位是一个局部变量）&#x20;
    > 9. 如果外部类和局部内部类的成员重名时，默认遵循就近原则，如果想访问外部类的成员，则可以使用（外部类名.this.成损）去访问

## 2.匿名内部类

*   基本介绍

    [goto：AnonymousInnerClass.java](https://gitee.com/jia-yan\_dong/code/blob/master/Java/javacode/chapter10/src/com/hspedu/ineerclass/AnonymousInnerClass.java)

    > 1. 该类没有名字，同时还是一个对象
    > 2. 匿名内部类是定义在外部类的局部位置，比如方法中，并且没有类名


*   注意事项和使用细节

    [goto：AnonymousInnerClassDetail.java](https://gitee.com/jia-yan\_dong/code/blob/master/Java/javacode/chapter10/src/com/hspedu/ineerclass/AnonymousInnerClassDetail.java)

    > 1. 匿名内部类的语法比较奇特，因为匿名内部类既是一个类的定义，同时它本身也是一个对象，因此从语法上看，它既有定义类的特征，也有创建对象的征，对前面代码分析可以看出这个特点，因此可以调用匿名内部类方法
    > 2. 可以直接访问外部类的所有成员，包含私有的
    > 3. 不能添加访问修饰符，因为它的地位就是一个局部变量
    > 4. 作用域：仅仅在定义它的方法或代码块中
    > 5. 匿名内部类--访问-->外部类成员\[访问方式：直接访问]
    > 6. 外部其他类--不能访问-->匿名内部类（因为匿名内部类地位是一个局部变量）&#x20;
    > 7. 如果外部类和匿名内部类的成员重名时，匿名内部类访问的话，默认遵循就近原则如果想访问外部类的成员，则可以使用（外部类名this.成员）去访问


*   匿名内部类的最佳实践

    [goto：InnerClassExercise01.java](https://gitee.com/jia-yan\_dong/code/blob/master/Java/javacode/chapter10/src/com/hspedu/ineerclass/InnerClassExercise01.java)

    > 当做实参直接传递，简洁高效

## 3.成员内部类

*   基本介绍

    [goto：MemberInnerClass01.java](https://gitee.com/jia-yan\_dong/code/blob/master/Java/javacode/chapter10/src/com/hspedu/ineerclass/MemberInnerClass01.java)

    > 1. 成员内部类是定义在外部类的成员位置，并且没有static修饰
    > 2. 可以直接访问外部类的所有成员，包含私有的
    > 3. 作用域和外部类的其他成员一样，为整个类体比如前面案例，在外部类的成员方法中创建成员内部类对象，再调用方法
    > 4. 成员内部类--访问-->外部类成员（比如属性)\[访问方式：直接访问]
    > 5. 外部类--访问--->成员内部类访问方式：创建对象，再访问&#x20;
    > 6. 外部其他类--访问-->成员内部类
    > 7. 如果外部类和内部类的成员重名时，内部类访问的话，默认遵循就近原则，如果想访问外部类的成员，则可以使用(外部类名.this.成员)去访问

## 4.静态内部类

*   基本介绍

    [goto：StaticInnerClass01.java](https://gitee.com/jia-yan\_dong/code/blob/master/Java/javacode/chapter10/src/com/hspedu/ineerclass/StaticInnerClass01.java)

    > 1. 静态内部类是定义在外部类的成员位置，并且有static修饰
    > 2. 可以直接访问外部类的所有静态成员，包含私有的，但不能直接访问非静态成员
    > 3. 可以添加任意访问修饰符(public、.protected、默认、private),因为它的地位就是一个成员
    > 4. 作用域：同其他的成员，为整个类体 4.静态内部类--访问-->外部类（比如：静态属性）\[访问方式：直接访问所有静态成员]
    > 5. 外部类-访问--->静态内部类访问方式：创建对象，再访问&#x20;
    > 6. 外部其他类--访问--->静态内部类&#x20;
    > 7. 如果外部类和静态内部类的成员重名时，静态内部类访问的时，默认遵循就近原则，如果想访问外部类的成员，则可以使用（外部类名.成员）去访问
