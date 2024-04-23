# 构造方法/构造器

*   基本说明

    [goto：Constructor01.java](https://gitee.com/jia-yan\_dong/code/blob/master/Java/javacode/chapter07/Constructor01.java)

    > 1. 构造方法又叫构造器(constructor)，是类的一种特殊的方法，它的主要作用是完成对新对象的初始化
    > 2. 构造器的修饰符可以默认，也可以是public protected private&#x20;
    > 3. 构造器没有返回值&#x20;
    > 4. 方法名和类名字必须一样&#x20;
    > 5. 参数列表和成员方法一样的规则 5)构造器的调用，由系统完成
*   注意事项和使用细节

    [goto：ConstructorDetail.java](https://gitee.com/jia-yan\_dong/code/blob/master/Java/javacode/chapter07/ConstructorDetail.java)

    > 1. 一个类可以定义多个不同的构造器，即构造器重载比如：我们可以再给Person类定义一个构造器，用来创建对象的时候，只指定人名不需要指定年龄
    > 2. 构造器名和类名要相同
    > 3. 构造器没有返回值
    > 4. 构造器是完成对象的初始化，并不是创建对象
    > 5. 在创建对象时，系统自动的调用该类的构造方法
    > 6. 如果程序员没有定义构造器，系统会自动给类生成一个默认无参构造器（也叫默认构造器)，比如Dog(){},使用javap指令反编译看看
    > 7. 一旦定义了自己的构造器，默认的构造器就覆盖了，就不能再使用默认的无参构造器，除非显式的定义一下，即：Dog(){}写（这点很重要）


*   javap的使用

    > 1. javap是JDK提供的一个命令行工具,javap能对给定的class文件提供的字节代码进行反编译
    > 2. 通过它，可以对照源代码和字节码，从而了解很多编译器内部的工作,对更深入地理解如何提高程序执行的效率等问题有极大的帮助
    > 3. 使用格式
    >    1. javap \<options> \<classes>
    >    2. 常用: javap -c -v 类名
    > 4.
    >
    >     |           指令           |                 作用                 |
    >     | :--------------------: | :--------------------------------: |
    >     |   -help  --help  -?    |               输出此用法消息              |
    >     |         -version       |                版本信息                |
    >     |       -v  -verbose     |               输出附加信息               |
    >     |            -l          |             输出行号和本地变量表             |
    >     |         -public        |              仅显示公共类和成员             |
    >     |       -protected       |            显示受保护的/公共类和成员           |
    >     |        -package        |       显示程序包/受保护的/公共类和成员 (默认)       |
    >     |      -p  -private      |              显示所有类和成员              |
    >     |           -c           |              对代码进行反汇编              |
    >     |           -s           |              输出内部类型签名              |
    >     |        -sysinfo        | 显示正在处理的类的系统信息 (路径, 大小, 日期, MD5 散列) |
    >     |       -constants       |               显示最终常量               |
    >     |   -classpath \<path>   |            指定查找用户类文件的位置            |
    >     |       -cp \<path>      |            指定查找用户类文件的位置            |
    >     | -bootclasspath \<path> |             覆盖引导类文件的位置             |

