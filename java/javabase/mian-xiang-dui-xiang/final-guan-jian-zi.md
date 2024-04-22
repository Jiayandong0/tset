# final关键字

[goto：final\_](https://gitee.com/jia-yan\_dong/code/tree/master/Java/javacode/chapter10/src/com/hspedu/final\_)

*   基本介绍

    [goto：Final01.java](https://gitee.com/jia-yan\_dong/code/blob/master/Java/javacode/chapter10/src/com/hspedu/final\_/Final01.java)

    > 1. final可以修饰类、属性、方法和局部变量
    > 2. 在某些情况下，可能有以下需求，就会使用到final:&#x20;
    >    1. 当不希望类被继承时，可以用final修饰.
    >    2. 当不希望父类的某个方法被子类覆盖/重写(override)时，可以用final关键字修饰
    >    3. 当不希望类的的某个属性的值被修改，可以用final修饰.
    >    4. 当不希望某个局部变量被修改，可以使用final修饰


*   注意事项和使用细节

    [goto：FinalDetail01.java](https://gitee.com/jia-yan\_dong/code/blob/master/Java/javacode/chapter10/src/com/hspedu/final\_/FinalDetail01.java) [goto：FinalDetail02.java](https://gitee.com/jia-yan\_dong/code/blob/master/Java/javacode/chapter10/src/com/hspedu/final\_/FinalDetail02.java)

    > 1. final修饰的属性又叫常量，一般用XX\_XX XX来命名&#x20;
    > 2. fina修饰的属性在定义时，必须赋初值，并且以后不能再修改，赋值可以在如下位置之一【选择一个位置赋初值即可】：
    >    1. 定义时：如public final double TAX RATE=0.08;
    >    2. 在构造器中
    >    3. 在代码块中
    > 3. 如果final修饰的属性是静态的，则初始化的位置只能是
    >    1. 定义时
    >    2. 在静态代码块不能在构造器中赋值&#x20;
    > 4. final类不能继承，但是可以实例化对象。\[A2类]
    > 5. 如果类不是final类，但是含有final方法，则该方法虽然不能重写，但是可以被继承。\[A3类]
    > 6. 一般来说，如果一个类已经是final类了，就没有必要再将方法修饰成final方法&#x20;
    > 7. final不能修饰构造方法（即构造器）
    > 8. final和static往往搭配使用，效率更高，不会导致类加载.底层编译器做了优化处理。
    > 9. 包装类(Integer、Double、Float、Boolean等都是final),String也是final类
