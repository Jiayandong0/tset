# 枚举

[goto：enum\_](https://gitee.com/jia-yan\_dong/code/tree/master/Java/javacode/chapter11/src/com/hspedu/enum\_)

*   基本介绍

    > 1. 枚举是一组常量的集合
    > 2. 枚举属于一种特殊的类，里面只包含一组有限的特定的对象


* 枚举的二种实现方式
  1.  自定义类实现枚举

      [goto：Enumeration02.java](https://gitee.com/jia-yan\_dong/code/blob/master/Java/javacode/chapter11/src/com/hspedu/enum\_/Enumeration02.java)

      > 1. 不需要提供setXxx方法，因为枚举对象值通常为只读
      > 2. 对枚举对象/属性使用final+static共同修饰，实现底层优化
      > 3. 枚举对象名通常使用全部大写，常量的命名规范
      > 4. 枚举对象根据需要，也可以有多个属性


  2.  使用 enum 关键字实现枚举

      [goto：Enumeration03.java](https://gitee.com/jia-yan\_dong/code/blob/master/Java/javacode/chapter11/src/com/hspedu/enum\_/Enumeration03.java)

      > 1. 当我们使用 enum 关键字开发一个枚举类时，默认会继承 Enum 类, 而且是一个 final 类
      > 2. 传统的 public static final Season2 SPRING = new Season2("春天", "温暖"); 简化成 SPRING("春天", "温暖")， 这里必须知道，它调用的是哪个构造器
      > 3. 如果使用无参构造器 创建 枚举对象，则实参列表和小括号都可以省略
      > 4. 当有多个枚举对象时，使用,间隔，最后有一个分号结尾
      > 5. 枚举对象必须放在枚举类的行首
*   enum 常用方法应用实例

    [goto：EnumMethod.java](https://gitee.com/jia-yan\_dong/code/blob/master/Java/javacode/chapter11/src/com/hspedu/enum\_/EnumMethod.java)



    |    方法名    |                 描述                 |
    | :-------: | :--------------------------------: |
    |  toString |        Enum 类已经重写过了，返回的是当前对象       |
    |    name   |         返回当前对象名（常量名）子类中不能重写        |
    |  ordinal  |         返回当前对象的位置号，默认从 0 开始        |
    |   values  |            返回当前枚举类中所有的常量           |
    |  valueOf  | 将字符串转换成枚举对象，要求字符串必须 为已有的常量名，否则报异常！ |
    | compareTo |          比较两个枚举常量，比较的就是编号！         |
