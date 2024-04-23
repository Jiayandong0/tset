# 变量

[goto：chapter03](https://gitee.com/jia-yan\_dong/code/tree/master/Java/javacode/chapter03)

## 1.变量的介绍

*   概念

    > 变量相当于内存中一个数据存储空间的表示，你可以把变量看做是一个房间的门牌号，通过门牌号我们可以找到房间，而通过变量名可以访问到变量(值)


*   使用注意事项

    [goto：VarDetail.java](https://gitee.com/jia-yan\_dong/code/tree/master/Java/javacode/chapter03/VarDetail.java)

    > * 变量表示内存中的一个存储区域\[不同的变量，类型不同，占用的空间大小不同比如：int4个字节，double就是8个字节]
    > * 该区域有自己的名称\[变量名]和类型\[数据类型]
    > * 变量必须先声明，后使用，即有顺序
    > * 该区域的数据/值可以在**同一类型**范围内不断变化
    > * 变量在同一个作用域内不能重名
    > * 变量=**变量名**+**值**+**数据类型**，这一点请大家注意。变量**三要素**



## 2.数据类型

*   基本介绍

    > * 每一种数据都定义了明确的数据类型，在内存中分配了不同大小的内存空间(字节)


*   分类一览图



    <figure><img src="../../.gitbook/assets/image (6).png" alt=""><figcaption></figcaption></figure>

    > 1. java 数据类型分为两大类 基本数据类型， 引用类型
    > 2. 基本数据类型有 8 中 数值型 \[byte , short , int , long , float ,double] char , boolean
    > 3. 引用类型 \[类，接口， 数组]

### 1.整型类型

[goto：IntDetail.java](https://gitee.com/jia-yan\_dong/code/blob/master/Java/javacode/chapter03/IntDetail.java)

|      类型      | 占用存储空间 |                        范围                       |
| :----------: | :----: | :---------------------------------------------: |
|  byte \[字节]  |   1字节  |                    -128\~127                    |
| short \[短整型] |   2字节  |      <p>-32768~32767<br>-2**15~2**15-1</p>      |
|   int \[整型]  |   4字节  | <p>-2147483648~2147483647<br>-2**31~2**31-1</p> |
|  long \[长整型] |   8字节  |               -2\*\*63\~2\*\*63-1               |

### 2.浮点类型

[goto：FloatDetail.java](https://gitee.com/jia-yan\_dong/code/blob/master/Java/javacode/chapter03/FloatDetail.java)

*   基本介绍

    > Java 的浮点类型可以表示一个小数，比如 123.4 、0.12、.2 等等


*   分类



    |       类型      | 占用存储空间 |          范围         |
    | :-----------: | :----: | :-----------------: |
    |  float \[单精度] |   4字节  |  -3.40E38\~3.40E38  |
    | double \[双精度] |   8字节  | -1.79E308\~1.79E308 |
*   说明一下

    > 1. 关于浮点数在机器中存放形式的简单说明,浮点数=符号位+指数位+尾数位
    > 2. 尾数部分可能丢失，造成精度损失(小数都是近似值)。
    > 3.  浮点型常量有两种表示形式
    >
    >     十进制数形式：5.12 512.0f.512(必须有小数点)
    >
    >     科学计数法形式：5.12e2\[5.12\*10的2次方] 5.12E-2\[5.12/10的2次方]
    > 4. [浮点型使用细节：FloatDetail.java](https://gitee.com/jia-yan\_dong/code/tree/master/Java/javacode/chapter03/FloatDetail.java)

### 3.字符类型

[goto：CharDetail.java](https://gitee.com/jia-yan\_dong/code/blob/master/Java/javacode/chapter03/CharDetail.java)

*   基本介绍&#x20;

    > 字符类型可以表示单个字符,字符类型是 char，char 是两个字节(可以存放汉字)，多个字符我们用字符串 String


*   字符类型使用细节

    > 1. ava中允许使用转义字符'\\'来将其后的字符转变为特殊字符型常量。例如：char c3='\n';
    > 2. 在java中，char的本质是一个整数，在输出时，是 unicode码对应的字符。&#x20;
    > 3. 可以直接给char赋一个整数，然后输出时，会按照对应的unicode字符输出\[97->a]&#x20;
    > 4. char类型是可以进行运算的，相当于一个整数，因为它都对应有Unicode码


*   字符编码

    > * ASCII(ASCI川编码表一个字节表示，一个128个字符，实际上一个字节可以表示256个字符，只用128个)&#x20;
    > * Unicode(Unicode编码表固定大小的编码使用两个字节来表示字符，字母和汉字统一都是占用两个字节，这样浪费空间)&#x20;
    > * utf-8(编码表，大小可变的编码字母使用1个字节，汉字使用3个字节)&#x20;
    > * gbk(可以表示汉字，而且范围广，字母使用1个字节，汉字2个字节)&#x20;
    > * gb2312(可以表示汉字，gb2312 < gbk)&#x20;
    > * big5码（繁体中文，台湾，香港）

### 4.boolean类型

[goto：Boolean01.java](https://gitee.com/jia-yan\_dong/code/blob/master/Java/javacode/chapter03/Boolean01.java)

*   基本介绍

    > * 布尔类型也叫boolean类型，booolean类型数据只允许取值true和false,无 null&#x20;
    > * boolean类型占1个字节

## 3.基本数据类型转换

### 1.自动类型转换

*   基本介绍

    [goto：AutoConvert.java](https://gitee.com/jia-yan\_dong/code/blob/master/Java/javacode/chapter03/AutoConvert.java)

    > 当ava程序在进行赋值或者运算时，精度小的类型自动转换为精度大的数据类型，这个就是<mark style="color:yellow;">**自动类型转换**</mark>


*   数据类型按精度(容量)大小排序为

    > * char -> int -> long -> float -> double
    > * byte -> short -> int -> long -> float -> double


*   自动类型转换注意和细节

    [goto：AutoConvertDetail.java](https://gitee.com/jia-yan\_dong/code/tree/master/Java/javacode/chapter03/AutoConvertDetail.java)

    > 1. 有多种类型的数据混合运算时，系统首先自动将所有数据 转换成容量最大的那种数据类型，然后再进行计算。
    > 2. 当我们把精度（容量）大的数据类型赋值给精度（容量）小的数据类型时，就会报错，反之就会进行自动类型转换。
    > 3. (byte、short)和char之间不会相互自动转换。
    > 4. &#x20;byte,short,char他们三者可以计算，在计算时首先转换为int类型。
    > 5. &#x20;boolean不参与转换
    > 6. 自动提升原则：表达式结果的类型自动提升为操作数中最大的类型&#x20;

### 2.强制类型转换

*   基本介绍

    [goto：ForceConvert.java](https://gitee.com/jia-yan\_dong/code/blob/master/Java/javacode/chapter03/AutoConvert.java)

    > 自动类型转换的逆过程，**将容量大的数据类型转换为容量小的数据类型**。使用时要加上强制转换符 ( )，但可能造成**精度降低或溢出**,格外要注意


*   强制类型转换细节说明

    [goto：ForceConvertDetail.java](https://gitee.com/jia-yan\_dong/code/tree/master/Java/javacode/chapter03/AutoConvertDetail.java)

    > 1. 当进行数据的大小从大 -> 小，就需要使用到强制转换
    > 2. 强转符号只针对于最近的操作数有效，往往会使用小括号提升优先级
    > 3. char类型可以保存int的常量值，但不能保存int的变量值需要强转
    > 4. byte和short、char类型在进行运算时，当做int类型处理。&#x20;
