# 理解main方法

[goto：main\_](https://gitee.com/jia-yan\_dong/code/tree/master/Java/javacode/chapter10/src/com/hspedu/main\_)

*   基本介绍

    > 1. main方法时虚拟机调用&#x20;
    > 2. java虚拟机需要调用类的main()方法，所以该方法的访问权限必须是public&#x20;
    > 3. java虚拟机在执行main()方法时不必创建对象，所以该方法必须是static&#x20;
    > 4. 该方法接收String类型的数组参数，该数组中保存执行java命令时传递给所运行的类的参数


*   特别提示

    [goto：Main01.java](https://gitee.com/jia-yan\_dong/code/blob/master/Java/javacode/chapter10/src/com/hspedu/main\_/Main01.java)

    > 1. 在 main()方法中，我们可以直接调用 main 方法所在类的静态方法或静态属性。
    > 2. 但是，不能直接访问该类中的非静态成员，必须创建该类的一个实例对象后，才能通过这个对象去访问类中的非静 态成员
