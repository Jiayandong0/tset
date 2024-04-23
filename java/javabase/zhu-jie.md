# 注解

[goto：annotation\_](https://gitee.com/jia-yan\_dong/code/tree/master/Java/javacode/chapter11/src/com/hspedu/annotation\_)

*   注解的理解

    > 1. 注解(Annotation)也被称为元数据(Metadata)，用于修饰解释 包、类、方法、属性、构造器、局部变量等数据信息
    > 2. 和注释一样，注解不影响程序逻辑，但注解可以被编译或运行，相当于嵌入在代码中的补充信息
    > 3. 在 JavaSE 中，注解的使用目的比较简单，例如标记过时的功能，忽略警告等。在 JavaEE 中注解占据了更重要的角 色，例如用来配置应用程序的任何切面，代替 java EE 旧版中所遗留的繁冗代码和 XML 配置等


*   基本的Annotation介绍

    > * 使用 Annotation 时要在其前面增加 @ 符号, 并把该 Annotation 当成一个修饰符使用。用于修饰它支持的程序元 素 三个基本的 Annotation:
    >   1. @Override: 限定某个方法，是重写父类方法, 该注解只能用于方法 [goto：Override\_.java](https://gitee.com/jia-yan\_dong/code/blob/master/Java/javacode/chapter11/src/com/hspedu/annotation\_/Override\_.java)
    >   2. @Deprecated: 用于表示某个程序元素(类, 方法等)已过时 [goto：Deprecated\_.java](https://gitee.com/jia-yan\_dong/code/blob/master/Java/javacode/chapter11/src/com/hspedu/annotation\_/Deprecated\_.java)
    >   3. @SuppressWarnings: 抑制编译器警告 [goto：SuppressWarnings.java](https://gitee.com/jia-yan\_dong/code/blob/master/Java/javacode/chapter11/src/com/hspedu/annotation\_/SuppressWarnings\_.java)


*   JDK 的元Annotation元注解

    > 1. JDK 的元 Annotation 用于修饰其他 Annotation
    >    1. @Retention 注解 <mark style="color:yellow;">**指定注解的作用范围，三种 SOURCE,CLASS,RUNTIME**</mark>
    >       1. 只能用于修饰一个 Annotation 定义, 用于指定该 Annotation 可以保留多长时间, @Rentention 包含一个 RetentionPolicy 类型的成员变量, 使用 @Rentention 时必须为该 value 成员变量指定值
    >       2. @Retention 的三种值
    >          1. RetentionPolicy.SOURCE: 编译器使用后，直接丢弃这种策略的注释&#x20;
    >          2. RetentionPolicy.CLASS: 编译器将把注解记录在 class 文件中. 当运行 Java 程序时, JVM 不会保留注解。 这是默认值
    >          3. RetentionPolicy.RUNTIME:编译器将把注解记录在 class 文件中. 当运行 Java 程序时, JVM 会保留注解. 程序可以 通过反射获取该注解
    >    2. @Target <mark style="color:yellow;">**指定注解可以在哪些地方使用**</mark>
    >       1. 用于修饰Annotation定义，用于指定被修饰的Annotation能用于修饰哪些程序元素
    >       2. @Target也包含一个名为value的成员变量。
    >    3. @Documented <mark style="color:yellow;">**指定该注解是否会在 javadoc 体现**</mark>
    >       1. 用于指定被该元Annotation修饰的Annotation类将被 javadoc工具提取成文档，即在生成文档时，可以看到该注解。
    >       2. 说明：定义为@Documented的注解必须设置Retention值为RUNTIME。
    >    4. @Inherited <mark style="color:yellow;">**子类会继承父类注解**</mark>
    >       1. 被它修饰的Annotation将具有继承性如果某个类使用了被@Inherited修饰的Annotation,则其子类将自动具有该注解
    >       2. 说明：实际应用中，使用较少，了解即可。
    > 2. 元注解本身作用不大，原因希望看源码时，可以知道他是干什么.
