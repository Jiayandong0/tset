# 运算符介绍

## 1.算术运算符

*   基本介绍

    > 算术运算符是对数值类型的变量进行运算的，在 Java 程序中使用的非常多


*   算术运算符一览



    <table><thead><tr><th align="center">运算符</th><th width="226" align="center">运算</th><th align="center">范例</th><th align="center">结果</th></tr></thead><tbody><tr><td align="center">+</td><td align="center">正号</td><td align="center">+7</td><td align="center">7</td></tr><tr><td align="center">-</td><td align="center">负号</td><td align="center">b=11;-b</td><td align="center">-11</td></tr><tr><td align="center">+</td><td align="center">加</td><td align="center">9+9</td><td align="center">18</td></tr><tr><td align="center">-</td><td align="center">减</td><td align="center">10-8</td><td align="center">2</td></tr><tr><td align="center">*</td><td align="center">成</td><td align="center">7*8</td><td align="center">56</td></tr><tr><td align="center">/</td><td align="center">除</td><td align="center">9/9</td><td align="center">1</td></tr><tr><td align="center">%</td><td align="center">取模</td><td align="center">11%9</td><td align="center">2</td></tr><tr><td align="center">++<br>++</td><td align="center">自增(前)：先运算后取值<br>自增(后)：先取值后运算</td><td align="center">a=2;b=++a;<br>a=2;b=a++;</td><td align="center">a=3;b=3;<br>a=3;b=2;</td></tr><tr><td align="center">--<br>--</td><td align="center">自减(前)：先运算后取值<br>自减(后)：先取值后运算</td><td align="center">a=2;b=--a;<br>a=2;b=a--;</td><td align="center">a=1;b=1;<br>a=1;b=2;</td></tr><tr><td align="center">+</td><td align="center">字符串相加</td><td align="center">"hello"+"world"</td><td align="center">"helloworld"</td></tr></tbody></table>
*   细节说明

    > 1. 对于除号"/"，它的整数除和小数除是有区别的：整数之间做除法时，只保留整数部分而舍弃小数部分。例如：int x=10/3,结果是3
    > 2. 当对一个数取模时，可以等价a%b=a-a/b\*b，这样我们可以看到取模的一个本质运算



## 2.关系运算符

*   基本介绍

    > 1. 关系运算符的结果都是 boolean 型，也就是要么是 true，要么是 false&#x20;
    > 2. 关系表达式 经常用在 if 结构的条件中或循环结构的条件中


*   关系运算符一览



    <table><thead><tr><th align="center">运算符</th><th width="226" align="center">运算</th><th width="209" align="center">范例</th><th align="center">结果</th></tr></thead><tbody><tr><td align="center">==</td><td align="center">相等于</td><td align="center">8==7</td><td align="center">false</td></tr><tr><td align="center">!=</td><td align="center">不等于</td><td align="center">8!=7</td><td align="center">true</td></tr><tr><td align="center">&#x3C;</td><td align="center">小于</td><td align="center">8&#x3C;7</td><td align="center">false</td></tr><tr><td align="center">></td><td align="center">大于</td><td align="center">8>7</td><td align="center">true</td></tr><tr><td align="center">&#x3C;=</td><td align="center">小于等于</td><td align="center">8&#x3C;=7</td><td align="center">false</td></tr><tr><td align="center">>=</td><td align="center">大于等于</td><td align="center">8>=7</td><td align="center">true</td></tr><tr><td align="center">instanceof</td><td align="center">检查是否是类的对象</td><td align="center">"hello" instanceof String </td><td align="center">true</td></tr></tbody></table>

## 3.逻辑运算符

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


*   && 和 & 使用区别

    > 1. &&短路与：如果第一个条件为 false，则第二个条件不会判断，最终结果为 false，效率高
    > 2. & 逻辑与：不管第一个条件是否为 false，第二个条件都要判断，效率低
    > 3. 开发中， 我们使用的基本是使用短路与&&, 效率高


*   || 和 | 使用区别

    > 1. ||短路或：如果第一个条件为 true，则第二个条件不会判断，最终结果为 true，效率高
    > 2. \| 逻辑或：不管第一个条件是否为 true，第二个条件都要判断，效率低
    > 3. 开发中，我们基本使用 ||



## 4.赋值运算符

*   基本赋值运算符

    > \=：int a = 10;


*   复合赋值运算符

    > \+= ，-= ，\*= ， /= ，%= 等


*   赋值运算符特点

    > 1. 运算顺序从右往左 int num = a + b + c;&#x20;
    > 2. 赋值运算符的左边 只能是变量,右边 可以是变量、表达式、常量值 int num = 20; int num2= 78 \* 34 - 10; int num3 = a;
    > 3. 复合赋值运算符等价于下面的效果 比如：a+=3;等价于 a=a+3; 其他类推
    > 4. 复合赋值运算符会进行类型转换



## 5.三元运算符

*   基本语法

    > 条件表达式 ? 表达式 1: 表达式 2;


*   运算规则

    > 1. 如果条件表达式为 true，运算后的结果是表达式 1；
    > 2. 如果条件表达式为 false，运算后的结果是表达式 2；



## 6.位运算符

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

## 7.运算符的优先级

*   基本介绍

    > 1. 运算符有不同的优先级，所谓优先级就是表达式运算中的运算顺序。如右表，上一行运算符总优先于下一行
    > 2. 只有单目运算符、赋值运算符是从右向左运算的
*   一览表



    <table data-header-hidden><thead><tr><th width="123"></th><th></th></tr></thead><tbody><tr><td></td><td>.    ()    {}    ;</td></tr><tr><td>R -> L</td><td>++    --    ~    !(data type)</td></tr><tr><td>L -> R</td><td>*    /    %</td></tr><tr><td>L -> R</td><td>+    -</td></tr><tr><td>L -> R</td><td>&#x3C;&#x3C;    >>    >>>    位移</td></tr><tr><td>L -> R</td><td>&#x3C;    >    &#x3C;=    >=    instanceof</td></tr><tr><td>L -> R</td><td>==    !=</td></tr><tr><td>L -> R</td><td>&#x26;    &#x26;&#x26;    |    ||    </td></tr><tr><td>L -> R</td><td>?    :</td></tr><tr><td>R -> L</td><td>=    *=    /=    %=    +=    -=    &#x3C;&#x3C;=    >>=    >>>=    &#x26;=    ^=    |=</td></tr></tbody></table>

