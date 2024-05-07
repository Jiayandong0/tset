# 异常

[goto：chapter12](https://gitee.com/jia-yan\_dong/code/tree/master/Java/javacode/chapter12)

## 1.异常介绍

*   基本介绍

    > 1. Java语言中，将程序执行中发生的不正常情况称为“异常”（开发过程中的语法错误和逻辑错误不是异常)
    > 2. 执行过程中所发生的异常事件可分为两大类&#x20;
    >    1. Error(错误)：Java虚拟机无法解决的严重问题。如：JVM系统内部错误、资源耗尽等严重情况。比如：StackOverflowError\[栈溢出]和OOM(out of memory),Error是严重错误，程序会崩溃
    >    2. Exception:其它因编程错误或偶然的外在因素导致的一般性问题，可以使用针对性的代码进行处理。例如空指针访问，试图读取不存在的文件，网络连接中断等等，Exception分为两大类：运行时异常程序运行时，发生的异常]和编译时异常\[编程时，编译器检查出的异常]


*   异常的分类

    > 1. 异常分为两大类，运行时异常和编译时异常&#x20;
    > 2. 运行时异常，编译器检查不出来。一般是指编程时的逻辑错误，是程序员应该避免其出现的异常。java.lang.RuntimeException类及它的子类都是运行时异常 对于运行时异常，可以不作处理，因为这类异常很普遍，若全处理可能会对程序的可读性和运行效率产生影响
    > 3. 编译时异常，是编译器要求必须处置的异常。



## 2.异常捕获

*   try-catch

    goto：[TryCatchDetail.java](https://gitee.com/jia-yan\_dong/code/blob/master/Java/javacode/chapter12/src/com/hspedu/try\_/TryCatchDetail.java)  [TryCatchDetail02.java ](https://gitee.com/jia-yan\_dong/code/blob/master/Java/javacode/chapter12/src/com/hspedu/try\_/TryCatchDetail02.java)[TryCatchDetail03.java](https://gitee.com/jia-yan\_dong/code/blob/master/Java/javacode/chapter12/src/com/hspedu/try\_/TryCatchDetail03.java)

    > 1. 如果异常发生了，则异常发生后面的代码不会执行，直接进入到catch块.
    > 2. 如果异常没有发生，则顺序执行try的代码块，不会进入到catch.
    > 3. 如果希望不管是否发生异常，都执行某段代码（比如关闭连接，释放资源等）则使用如下代码-finally{}
    > 4. 可以有多个catch语句，捕获不同的异常（进行不同的业务处理），要求父类异常在后，子类异常在前，比如(Exception在后，NullPointerException在前)，如果发生异常，只会匹配一个catch
    > 5. 可以进行try-finally配合使用，这种用法相当于没有捕获异常，因此程序会直接崩掉/退出。应用场景，就是执行一段代码，不管是否发生异常，都必须执行某个业务逻辑


*   throws

    [goto：ThrowsDetail.java](https://gitee.com/jia-yan\_dong/code/blob/master/Java/javacode/chapter12/src/com/hspedu/throws\_/ThrowsDetail.java)

    > 1. 如果一个方法（中的语句执行时）可能生成某种异常，但是并不能确定如何处理这种异常，则此方法应显示地声明抛出异常，表明该方法将不对这些异常进行处理，而由该方法的调用者负责处理。
    > 2. 在方法声明中用throws语句可以声明抛出异常的列表，throws后面的异常类型可以是方法中产生的异常类型，也可以是它的父类。
    > 3. 对于编译异常，程序中必须处理，比如try-catch或者throws&#x20;
    > 4. 对于运行时异常，程序中如果没有处理，默认就是throws的方式处理
    > 5. 子类重写父类的方法时，对抛出异常的规定：子类重写的方法，所抛出的异常类型要么和父类抛出的异常一致，要么为父类抛出的异常的类型的子类型
    > 6. 在throws过程中，如果有方法try-catch,就相当于处理异常，就可以不必 throws



## 3.自定义异常

*   基本介绍

    > 当程序中出现了某些“错误”，但该错误信息并没有在Throwable子类中描述处理，这个时候可以自己设计异常类，用于描述该错误信息。


*   自定义异常的步骤

    [goto：CustomException.java](https://gitee.com/jia-yan\_dong/code/blob/master/Java/javacode/chapter12/src/com/hspedu/customexception\_/CustomException.java)

    > 1. 定义类：自定义异常类名（程序员自己写）继承Exception或RuntimeException
    > 2. 如果继承Exception,属于编译异常
    > 3. 如果继承RuntimeException,属于运行异常（一般来说，继承RuntimeException)
