# Object类详解

[goto：object\_](https://gitee.com/jia-yan\_dong/code/tree/master/Java/javacode/chapter08/src/com/hspedu/object\_)

## 1.equals

*   \==和 equals 的对比

    [goto：Equals01.java](https://gitee.com/jia-yan\_dong/code/blob/master/Java/javacode/chapter08/src/com/hspedu/object\_/Equals01.java)

    > 1. \==是一个比较运算符&#x20;
    > 2. \==既可以判断基本类型，又可以判断引用类型
    > 3. \==如果判断基本类型，判断的是值是否相等。示例：int i = 10; double d=10.0;
    > 4. \==如果判断引用类型，判断的是地址是否相等，即判定是不是同一个对象
    > 5. equals:是Object类中的方法，只能判断引用类型
    > 6. 默认判断的是地址是否相等，子类中往往重写该方法，用于判断内容是否相等。比如 Integer,String

## 2.hashCode

*   基本介绍

    [goto：HashCode\_.java](https://gitee.com/jia-yan\_dong/code/blob/master/Java/javacode/chapter08/src/com/hspedu/object\_/HashCode\_.java)

    > 1. 提高具有哈希结构的容器的效率
    > 2. 两个引用，如果指向的是同一个对象，则哈希值肯定是一样的！
    > 3. 两个引用，如果指向的是不同对象，则哈希值是不一样的
    > 4. &#x20;哈希值主要根据地址号来的！， 不能完全将哈希值等价于地址。

## 3.toString

*   基本介绍

    [goto：ToString\_.java](https://gitee.com/jia-yan\_dong/code/blob/master/Java/javacode/chapter08/src/com/hspedu/object\_/ToString.java)

    > 1. 默认返回：全类名+@+哈希值的十六进制,子类往往重写 toString 方法，用于返回对象的属性信息
    > 2. 重写 toString 方法，打印对象或拼接对象时，都会自动调用该对象的 toString 形式.
    > 3. 当直接输出一个对象时，toString 方法会被默认的调用, 比如 System.out.println(monster)； 就会默认调用 monster.toString()

## 4.finalize

*   基本介绍

    [goto：Finalize\_.java](https://gitee.com/jia-yan\_dong/code/blob/master/Java/javacode/chapter08/src/com/hspedu/object\_/Finalize.java)

    > 1. 当对象被回收时，系统自动调用该对象的 finalize 方法。子类可以重写该方法，做一些释放资源的操作
    > 2. 什么时候被回收：当某个对象没有任何引用时，则 jvm 就认为这个对象是一个垃圾对象，就会使用垃圾回收机制来 销毁该对象，在销毁该对象前，会先调用 finalize 方法
    > 3. 垃圾回收机制的调用，是由系统来决定(即有自己的 GC 算法), 也可以通过 System.gc() 主动触发垃圾回收机制
