# 访问修饰符

*   基本介绍

    [goto：.java](fang-wen-xiu-shi-fu.md#id-1.-cheng-yuan-fang-fa)

    > * java 提供四种访问控制修饰符号，用于控制方法和属性(成员变量)的访问权限（范围）
    >   1. 公开级别:用 public 修饰,对外公开
    >   2. 受保护级别:用 protected 修饰,对子类和同一个包中的类公开
    >   3. 默认级别:没有修饰符号,向同一个包的类公开
    >   4. 私有级别:用 private 修饰,只有类本身可以访问,不对外公开.


*   4 种访问修饰符的访问范围

    | 访问级别 |   访问修饰符   |  同类 |  同包 |  子类 | 不同包 |
    | :--: | :-------: | :-: | :-: | :-: | :-: |
    |  公开  |   public  |  ✅  |  ✅  |  ✅  |  ✅  |
    |  受保护 | protected |  ✅  |  ✅  |  ✅  |  ❌  |
    |  默认  |   没有修饰符   |  ✅  |  ✅  |  ❌  |  ❌  |
    |  私有的 |  private  |  ✅  |  ❌  |  ❌  |  ❌  |


*   注意事项和使用细节

    [goto：Test.java](https://gitee.com/jia-yan\_dong/code/blob/master/Java/javacode/chapter08/src/com/hspedu/modifier/Test.java)

    > 1. 修饰符可以用来修饰类中的属性，成员方法以及类
    > 2. 只有默认的和public:才能修饰类！，并且遵循上述访问权限的特点
    > 3. 成员方法的访问规则和属性完全一样.
