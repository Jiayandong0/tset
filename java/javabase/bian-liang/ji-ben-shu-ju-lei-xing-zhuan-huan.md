# 基本数据类型转换

## 1.自动类型转换

*   基本介绍 [goto：AutoConvert.java](https://gitee.com/jia-yan\_dong/code/blob/master/Java/javacode/chapter03/AutoConvert.java)

    > 当ava程序在进行赋值或者运算时，精度小的类型自动转换为精度大的数据类型，这个就是<mark style="color:yellow;">**自动类型转换**</mark>


*   数据类型按精度(容量)大小排序为

    > * char -> int -> long -> float -> double
    > * byte -> short -> int -> long -> float -> double


*   自动类型转换注意和细节 [goto：AutoConvertDetail.java](https://gitee.com/jia-yan\_dong/code/tree/master/Java/javacode/chapter03/AutoConvertDetail.java)

    > 1. 有多种类型的数据混合运算时，系统首先自动将所有数据 转换成容量最大的那种数据类型，然后再进行计算。
    > 2. 当我们把精度（容量）大的数据类型赋值给精度（容量）小的数据类型时，就会报错，反之就会进行自动类型转换。
    > 3. (byte、short)和char之间不会相互自动转换。
    > 4. &#x20;byte,short,char他们三者可以计算，在计算时首先转换为int类型。
    > 5. &#x20;boolean不参与转换
    > 6. 自动提升原则：表达式结果的类型自动提升为操作数中最大的类型&#x20;

## 2.强制类型转换

*   基本介绍 [goto：ForceConvert.java](https://gitee.com/jia-yan\_dong/code/blob/master/Java/javacode/chapter03/AutoConvert.java)

    > 自动类型转换的逆过程，**将容量大的数据类型转换为容量小的数据类型**。使用时要加上强制转换符 ( )，但可能造成**精度降低或溢出**,格外要注意


*   强制类型转换细节说明 [goto：ForceConvertDetail.java](https://gitee.com/jia-yan\_dong/code/tree/master/Java/javacode/chapter03/AutoConvertDetail.java)

    > 1. 当进行数据的大小从大 -> 小，就需要使用到强制转换
    > 2. 强转符号只针对于最近的操作数有效，往往会使用小括号提升优先级
    > 3. char类型可以保存int的常量值，但不能保存int的变量值需要强转
    > 4. byte和short、char类型在进行运算时，当做int类型处理。&#x20;
