# 运算符

[goto：**chapter04**](https://gitee.com/jia-yan\_dong/code/tree/master/Java/javacode/chapter04)

## 1.运算符

### 1.算术运算符

[goto：ArithmeticOperator.java](https://gitee.com/jia-yan\_dong/code/blob/master/Java/javacode/chapter04/ArithmeticOperator.java)

*   基本介绍

    > 算术运算符是对数值类型的变量进行运算的，在 Java 程序中使用的非常多


*   算术运算符一览



    <table><thead><tr><th align="center">运算符</th><th width="226" align="center">运算</th><th align="center">范例</th><th align="center">结果</th></tr></thead><tbody><tr><td align="center">+</td><td align="center">正号</td><td align="center">+7</td><td align="center">7</td></tr><tr><td align="center">-</td><td align="center">负号</td><td align="center">b=11;-b</td><td align="center">-11</td></tr><tr><td align="center">+</td><td align="center">加</td><td align="center">9+9</td><td align="center">18</td></tr><tr><td align="center">-</td><td align="center">减</td><td align="center">10-8</td><td align="center">2</td></tr><tr><td align="center">*</td><td align="center">成</td><td align="center">7*8</td><td align="center">56</td></tr><tr><td align="center">/</td><td align="center">除</td><td align="center">9/9</td><td align="center">1</td></tr><tr><td align="center">%</td><td align="center">取模</td><td align="center">11%9</td><td align="center">2</td></tr><tr><td align="center">++<br>++</td><td align="center">自增(前)：先运算后取值<br>自增(后)：先取值后运算</td><td align="center">a=2;b=++a;<br>a=2;b=a++;</td><td align="center">a=3;b=3;<br>a=3;b=2;</td></tr><tr><td align="center">--<br>--</td><td align="center">自减(前)：先运算后取值<br>自减(后)：先取值后运算</td><td align="center">a=2;b=--a;<br>a=2;b=a--;</td><td align="center">a=1;b=1;<br>a=1;b=2;</td></tr><tr><td align="center">+</td><td align="center">字符串相加</td><td align="center">"hello"+"world"</td><td align="center">"helloworld"</td></tr></tbody></table>
*   细节说明

    > 1. 对于除号"/"，它的整数除和小数除是有区别的：整数之间做除法时，只保留整数部分而舍弃小数部分。例如：int x=10/3,结果是3
    > 2. 当对一个数取模时，可以等价a%b=a-a/b\*b，这样我们可以看到取模的一个本质运算

### 2.关系运算符

[goto：RelationalOperator.java](https://gitee.com/jia-yan\_dong/code/blob/master/Java/javacode/chapter04/RelationalOperator.java)

*   基本介绍

    > 1. 关系运算符的结果都是 boolean 型，也就是要么是 true，要么是 false&#x20;
    > 2. 关系表达式 经常用在 if 结构的条件中或循环结构的条件中


*   关系运算符一览



    <table><thead><tr><th align="center">运算符</th><th width="226" align="center">运算</th><th width="209" align="center">范例</th><th align="center">结果</th></tr></thead><tbody><tr><td align="center">==</td><td align="center">相等于</td><td align="center">8==7</td><td align="center">false</td></tr><tr><td align="center">!=</td><td align="center">不等于</td><td align="center">8!=7</td><td align="center">true</td></tr><tr><td align="center">&#x3C;</td><td align="center">小于</td><td align="center">8&#x3C;7</td><td align="center">false</td></tr><tr><td align="center">></td><td align="center">大于</td><td align="center">8>7</td><td align="center">true</td></tr><tr><td align="center">&#x3C;=</td><td align="center">小于等于</td><td align="center">8&#x3C;=7</td><td align="center">false</td></tr><tr><td align="center">>=</td><td align="center">大于等于</td><td align="center">8>=7</td><td align="center">true</td></tr><tr><td align="center">instanceof</td><td align="center">检查是否是类的对象</td><td align="center">"hello" instanceof String </td><td align="center">true</td></tr></tbody></table>

### 3.逻辑运算符

*   基本介绍

    > 用于连接多个条件（多个关系表达式），最终的结果也是一个 boolean 值


*   逻辑运算符一览



    <table><thead><tr><th align="center">a</th><th width="226" align="center">b</th><th width="209" align="center">a&#x26;b</th><th align="center">a&#x26;&#x26;b</th><th align="center">a|b</th><th align="center">a||b</th><th align="center">!a</th><th align="center">a^b</th></tr></thead><tbody><tr><td align="center">true</td><td align="center">true</td><td align="center">true</td><td align="center">true</td><td align="center">true</td><td align="center">true</td><td align="center">false</td><td align="center">false</td></tr><tr><td align="center">true</td><td align="center">false</td><td align="center">false</td><td align="center">false</td><td align="center">true</td><td align="center">true</td><td align="center">false</td><td align="center">true</td></tr><tr><td align="center">false</td><td align="center">true</td><td align="center">false</td><td align="center">false</td><td align="center">true</td><td align="center">true</td><td align="center">true</td><td align="center">true</td></tr><tr><td align="center">false</td><td align="center">false</td><td align="center">false</td><td align="center">false</td><td align="center">false</td><td align="center">false</td><td align="center">true</td><td align="center">false</td></tr></tbody></table>
*   逻辑运算规则

    > 1. a\&b : & 叫逻辑与：规则：当 a 和 b 同时为 true ,则结果为 true, 否则为 false&#x20;
    > 2. a&\&b : && 叫短路与：规则：当 a 和 b 同时为 true ,则结果为 true,否则为 false&#x20;
    > 3. a|b : | 叫逻辑或，规则：当 a 和 b ，有一个为 true ,则结果为 true,否则为 false
    > 4. a||b : || 叫短路或，规则：当 a 和 b ，有一个为 true ,则结果为 true,否则为 false
    > 5. !a : 叫取反，或者非运算。当 a 为 true, 则结果为 false, 当 a 为 false 是，结果为 true
    > 6. a^b: 叫逻辑异或，当 a 和 b 不同时，则结果为 true, 否则为 false


*   && 和 & 使用区别  [goto：LogicOperator01.java](https://gitee.com/jia-yan\_dong/code/blob/master/Java/javacode/chapter04/LogicOperator01.java)&#x20;

    > 1. &&短路与：如果第一个条件为 false，则第二个条件不会判断，最终结果为 false，效率高
    > 2. & 逻辑与：不管第一个条件是否为 false，第二个条件都要判断，效率低
    > 3. 开发中， 我们使用的基本是使用短路与&&, 效率高


*   || 和 | 使用区别  [goto：LogicOperator02.java](https://gitee.com/jia-yan\_dong/code/blob/master/Java/javacode/chapter04/LogicOperator02.java)

    > 1. ||短路或：如果第一个条件为 true，则第二个条件不会判断，最终结果为 true，效率高
    > 2. \| 逻辑或：不管第一个条件是否为 true，第二个条件都要判断，效率低
    > 3. 开发中，我们基本使用 ||

### 4.赋值运算符

[goto：AssignOperator.java](https://gitee.com/jia-yan\_dong/code/blob/master/Java/javacode/chapter04/AssignOperator.java)

*   基本赋值运算符

    > \=：int a = 10;


*   复合赋值运算符

    > \+= ，-= ，\*= ， /= ，%= 等


*   赋值运算符特点

    > 1. 运算顺序从右往左 int num = a + b + c;&#x20;
    > 2. 赋值运算符的左边 只能是变量,右边 可以是变量、表达式、常量值 int num = 20; int num2= 78 \* 34 - 10; int num3 = a;
    > 3. 复合赋值运算符等价于下面的效果 比如：a+=3;等价于 a=a+3; 其他类推
    > 4. 复合赋值运算符会进行类型转换

### 5.三元运算符

goto：[TernaryOperator.java](https://gitee.com/jia-yan\_dong/code/tree/master/Java/javacode/chapter04/TernaryOperator.java) [TernaryOperatorDetail.java](https://gitee.com/jia-yan\_dong/code/blob/master/Java/javacode/chapter04/TernaryOperatorDetail.java)

*   基本语法

    > 条件表达式 ? 表达式 1: 表达式 2;


*   运算规则

    > 1. 如果条件表达式为 true，运算后的结果是表达式 1；
    > 2. 如果条件表达式为 false，运算后的结果是表达式 2；

### 6.位运算符

goto：[**Bitoperator.java**](https://gitee.com/jia-yan\_dong/code/blob/master/Java/javacode/chapter04/Bitoperator.java) [**Bitoperator02.java**](https://gitee.com/jia-yan\_dong/code/blob/master/Java/javacode/chapter04/BitOperator02.java)

* 一览表

|       运算符      |          运算规则          |
| :------------: | :--------------------: |
|      按位与 &     |     两位全为1，结果为1，否则为0    |
|     按位或 \|     |    两位有一个为1，结果为1，否则为0   |
|     按位异或 ^     |  两位一个为0，一个为1，结果为1，否则为0 |
|     按位取反\~     |      0 -> 1、1 -> 0     |
|     算术右移 >>    | 低位溢出,符号位不变,并用符号位补溢出的高位 |
|     算术左移 <<    |       符号位不变,低位补 0      |
| >>>逻辑右移也叫无符号右移 |       低位溢出，高位补 0       |

### 7.运算符的优先级

*   基本介绍

    > 1. 运算符有不同的优先级，所谓优先级就是表达式运算中的运算顺序。如右表，上一行运算符总优先于下一行
    > 2. 只有单目运算符、赋值运算符是从右向左运算的
*   一览表



    <table data-header-hidden><thead><tr><th width="123">执行顺序</th><th>符号</th></tr></thead><tbody><tr><td></td><td>.    ()    {}    ;</td></tr><tr><td>R -> L</td><td>++    --    ~    !(data type)</td></tr><tr><td>L -> R</td><td>*    /    %</td></tr><tr><td>L -> R</td><td>+    -</td></tr><tr><td>L -> R</td><td>&#x3C;&#x3C;    >>    >>>    位移</td></tr><tr><td>L -> R</td><td>&#x3C;    >    &#x3C;=    >=    instanceof</td></tr><tr><td>L -> R</td><td>==    !=</td></tr><tr><td>L -> R</td><td>&#x26;    &#x26;&#x26;    |    ||    </td></tr><tr><td>L -> R</td><td>?    :</td></tr><tr><td>R -> L</td><td>=    *=    /=    %=    +=    -=    &#x3C;&#x3C;=    >>=    >>>=    &#x26;=    ^=    |=</td></tr></tbody></table>

## 2.进制

*   进制介绍

    > * 对于整数，有四种表示方式
    > * 二进制：0,1 ，满 2 进 1.以 0b 或 0B 开头
    > * 十进制：0-9 ，满 10 进 1
    > * 八进制：0-7 ，满 8 进 1. 以数字 0 开头表示
    > * 十六进制：0-9 及 A(10)-F(15)，满 16 进 1. 以 0x 或 0X 开头表示。此处的 A-F 不区分大小写

### 1.二进制转换成十进制

*   规则

    > 从最低位（右边）开始，将每个位上的数提取出来，乘以2的（位数-1）次方，然后求和


*   案例：请将0b1011转成十进制的数&#x20;

    > 0b<mark style="color:blue;">1</mark><mark style="color:purple;">0</mark><mark style="color:red;">1</mark><mark style="color:yellow;">1</mark> = <mark style="color:blue;">1 \* 2的(1-1)次方</mark> + <mark style="color:red;">1\* 2的(2-1)次方</mark> + <mark style="color:purple;">0 \* 2的(3-1)次方</mark>+ <mark style="color:yellow;">1 \* 2的(4-1)次方法</mark>=<mark style="color:blue;">1</mark> + <mark style="color:purple;">2</mark> + <mark style="color:red;">0</mark> + <mark style="color:yellow;">8</mark> = 11

### 2.八进制转换成十进制

*   规则

    > 从最低位（右边）开始，将每个位上的数提取出来，乘以8的（位数-1）次方，然后求和
*   案例：请将0234转成十进制的数

    > &#x20;0234 = 4 \* 8^0 + 3\* 8 ^ 1 + 2 \* 8 ^ 2 = 4 + 24 + 128 = 156

### 3.十六进制转换成十进制

*   规则

    > 从最低位(右边)开始，将每个位上的数提取出来，乘以 16 的(位数-1)次方，然后求和
*   案例：请将 0x23A 转成十进制的数

    > 0x23A = 10 \* 16^0 + 3 \* 16 ^ 1 + 2 \* 16^2 = 10 + 48 + 512 = 570

### 4.十进制转换成二进制

*   规则

    > 将该数不断除以 2，直到商为 0 为止，然后将每步得到的余数倒过来，就是对应的二进制
*   案例：34 转成二进制 = 0B00100010

    > 34&#x20;
    >
    > \= 34 / 2 = 0
    >
    > \= 17 / 2 = 1
    >
    > \= 8 / 2 = 0&#x20;
    >
    > \= 4 / 2 = 0&#x20;
    >
    > \= 2 / 2 = 0&#x20;
    >
    > \= 1 / 2 = 1&#x20;

### 5.十进制转换成八进制

*   规则

    > 将该数不断除以 8，直到商为 0 为止，然后将每步得到的余数倒过来，就是对应的八进制
*   案例：请将 131 转成八进制 => 0203

    > 131&#x20;
    >
    > \= 131 / 8 = 3
    >
    > \= 16 / 8 = 0
    >
    > \= 2 / 8 = 2

### 6.十进制转换成十六进制

*   规则

    > 将该数不断除以 16，直到商为 0 为止，然后将每步得到的余数倒过来，就是对应的十六进制
*   案例：请将 237 转成十六进制 => 0xED

    > 237&#x20;
    >
    > \= 237 / 16 = 13 -> D
    >
    > \= 14 / 16 =14 ->  E

### 7.二进制转换成八进制

*   规则

    > 从低位开始,将二进制数每三位一组，转成对应的八进制数即可
*   案例：请将 ob11010101 转成八进制

    > ob11(3)010(2)101(5) => 0325

### 8.二进制转换成十六进制

*   规则

    > 从低位开始，将二进制数每四位一组，转成对应的十六进制数即可
*   案例：请将 ob11010101 转成十六进制

    > ob1101(D)0101(5) = 0xD5

### 9.八进制转换成二进制

*   规则

    > 将八进制数每 1 位，转成对应的一个 3 位的二进制数即可
*   案例：请将 0237 转成二进制

    > 02(010)3(011)7(111) = 0b10011111

### 10.十六进制转换成二进制

*   规则

    > 将十六进制数每 1 位，转成对应的 4 位的一个二进制数即可
*   案例：请将 0x23B 转成二进制

    > 0x2(0010)3(0011)B(1011) = 0b001000111011

## 3.位运算

### 1.二进制在运算中的说明

> 1. 二进制是逢2进位的进位制，0、1是基本算符
> 2. 现代的电子计算机技术全部采用的是二进制，因为它只使用0、1两个数字符号，非常简单方便，易于用电子方式实现。计算机内部处理的信息，都是采用二进制数来表示的。二进制(Binary)数用0和1两个数字及其组合来表示任何数。进位规则是"逢2进1”，数字1在不同的位上代表不同的值，按从右至左的次序，这个值以二倍递增。

### 2.原码、反码、补码

> 1. 二进制的最高位是符号位：0表示正数，1表示负数
> 2. 正数的原码，反码，补码都一样(三码合一)
> 3. 负数的反码=它的原码符号位不变，其它位取反(0->1,1->0)&#x20;
> 4. 负数的补码=它的反码+1，负数的反码=负数的补码-1&#x20;
> 5. 0的反码，补码都是0
> 6. java没有无符号数，换言之，java中的数都是有符号的
> 7. 在计算机运算的时候，都是以<mark style="color:yellow;">**补码的方式**</mark>来运算的.
> 8. 当我们看运算结果的时候，要看他的<mark style="color:yellow;">**原码**</mark>（重点）
