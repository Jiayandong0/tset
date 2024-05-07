# 程序控制结构

[goto：**chapter05**](https://gitee.com/jia-yan\_dong/code/tree/master/Java/javacode/chapter05)

## 1.判断控制

### 1.顺序控制

*   基本介绍

    > 程序从上到下逐行地执行，中间没有任何判断和跳转


*   流程图

    <figure><img src="../../.gitbook/assets/image (5).png" alt="" width="219"><figcaption></figcaption></figure>



### 2.分支控制 if-else

#### 1.单分支

[goto：If01.java](https://gitee.com/jia-yan\_dong/code/blob/master/Java/javacode/chapter05/If01.java)

*   基本语法

    {% code lineNumbers="true" %}
    ```java
    if(条件表达式){
        执行代码块;
    }
    ```
    {% endcode %}
*   流程图

    <figure><img src="../../.gitbook/assets/image (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

#### 2.双分支

[goto：If02.java](https://gitee.com/jia-yan\_dong/code/blob/master/Java/javacode/chapter05/If02.java)

*   基本语法

    {% code lineNumbers="true" %}
    ```java
    if(条件表达式){
        执行代码块1;
    }else{
        执行代码块2;
    }
    ```
    {% endcode %}
*   流程图

    <figure><img src="../../.gitbook/assets/image (2) (1).png" alt="" width="477"><figcaption></figcaption></figure>

#### 3.多分支

[goto：If03.java](https://gitee.com/jia-yan\_dong/code/blob/master/Java/javacode/chapter05/If03.java)

*   基本语法

    {% code lineNumbers="true" %}
    ```java
    if(条件表达式1){
        执行代码块1;
    }else if(条件表达式2){
        执行代码块2;
    }
    ....
    else{
        执行代码块n;
    }
    ```
    {% endcode %}
*   流程图

    <figure><img src="../../.gitbook/assets/image (4) (1).png" alt="" width="563"><figcaption></figcaption></figure>

#### 4.嵌套分支

[goto：NestedIf.java](https://gitee.com/jia-yan\_dong/code/blob/master/Java/javacode/chapter05/NestedIf.java)

*   基本介绍

    > 在一个分支结构中又完整的嵌套了另一个完整的分支结构，里面的分支的结构称为内层分支外面的分支结构称为外 层分支。建议: 不要超过 3 层 （可读性不好）
*   基本语法

    {% code lineNumbers="true" %}
    ```java
    if(){
      if(){
        if...else...
      }else{
        if...else...
      }
    }
    ```
    {% endcode %}

### 3.switch 分支结构

[goto：Switch01.java](https://gitee.com/jia-yan\_dong/code/blob/master/Java/javacode/chapter05/Switch01.java)

*   基本语法

    {% code lineNumbers="true" %}
    ```java
    switch(表达式){
        case 常量1:
        语句块;
        break;
        case 常量2:
        语句块;
        break;
        ...
        default:
        语句块;
        break;
    }
    ```
    {% endcode %}
*   流程图

    <figure><img src="../../.gitbook/assets/image (5) (1).png" alt="" width="563"><figcaption></figcaption></figure>


*   注意事项和细节讨论  [goto：SwitchDetail.java](https://gitee.com/jia-yan\_dong/code/blob/master/Java/javacode/chapter05/SwitchDetail.java)

    > 1. 表达式数据类型，应和case后的常量类型一致，或者是可以自动转成可以相互比较的类型，比如输入的是字符，而常量是int&#x20;
    > 2. switch(表达式)中表达式的返回值必须是：(byte、short、int、char、enum\[枚举]，String)
    > 3. case子句中的值必须是常量，而不能是变量&#x20;
    > 4. default子句是可选的，当没有匹配的case时，执行default&#x20;
    > 5. break语句用来在执行完一个case分支后使程序跳出switch语句块；如果没有写 break,程序会顺序执行到switch结尾，除非遇到break;


*   switch 和 if 的比较

    > 1. 如果判断的具体数值不多，而且符合 byte、 short 、int、 char, enum\[枚举], String 这 6 种类型。虽然两个语句都可 以使用，建议使用 swtich 语句
    > 2. 其他情况：对区间判断，对结果为 boolean 类型判断，使用 if，if 的使用范围更广

## 2.循环控制

### 1.for 循环控制

*   基本语法

    {% code lineNumbers="true" %}
    ```java
    for(循环变量初始化;循环条件;循环变量迭代){
        执行语句;
    }
    ```
    {% endcode %}
*   说明

    > 1. &#x20;for 关键字，表示循环控制&#x20;
    > 2. for 有四要素: (1)循环变量初始化(2)循环条件(3)循环操作(4)循环变量迭代
    > 3. 循环操作 , 这里可以有多条语句，也就是我们要循环执行的代码
    > 4. 如果 循环操作(语句) 只有一条语句，可以省略 {}, 建议不要省略


*   注意事项和细节说明

    [goto：ForDetail.java](https://gitee.com/jia-yan\_dong/code/blob/master/Java/javacode/chapter05/ForDetail.java)

    > 1. 循环条件是返回一个布尔值的表达式
    > 2. for(;循环判断条件;) 中的初始化和变量迭代可以写到其它地方，但是两边的分号不能省略
    > 3. 循环初始值可以有多条初始化语句，但要求类型一样，并且中间用逗号隔开，循环变量迭代也可以有多条变量迭代 语句，中间用逗号隔开

### 2.while 循环控制

[goto：While.java](https://gitee.com/jia-yan\_dong/code/blob/master/Java/javacode/chapter05/DoWhile01.java)

*   基本语法

    {% code lineNumbers="true" %}
    ```java
    循环变量初始化;
    while(循环条件){
        执行语句;
        循环变量迭代;
    }
    ```
    {% endcode %}
*   注意事项和细节说明

    > 1. 循环条件是返回一个布尔值的表达式
    > 2. while 循环是先判断再执行语句

### 3.do..while

[goto：DoWhile01.java](https://gitee.com/jia-yan\_dong/code/blob/master/Java/javacode/chapter05/DoWhile01.java)

*   基本语法

    {% code lineNumbers="true" %}
    ```java
    循环变量初始化;
    do{
        循环体(语句);
        循环变量迭代;
    }while(循环条件)
    ```
    {% endcode %}
*   注意事项和细节说明

    > 1. 循环条件是返回一个布尔值的表达式
    > 2. do..while 循环是先执行，再判断， 因此它至少执行一次

## 3.break、continue和return

### 1.break

[goto：Break01.java](https://gitee.com/jia-yan\_dong/code/blob/master/Java/javacode/chapter05/Break01.java)

*   基本介绍

    > break 语句用于终止某个语句块的执行，一般使用在 switch 或者循环\[for , while , do-while]中


*   细节 [goto：BreakDetail.java](https://gitee.com/jia-yan\_dong/code/blob/master/Java/javacode/chapter05/BreakDetail.java)

    > 1. break语句可以指定退出哪层&#x20;
    > 2. label1是标签，名字由程序员指定
    > 3. break后指定到哪个label就退出到哪里
    > 4. 在实际的开发中，尽量不要使用标签
    > 5. 如果没有指定break，默认退出最近的循环体

### 2.continue

goto：[Continue01.java](https://gitee.com/jia-yan\_dong/code/blob/master/Java/javacode/chapter05/Continue01.java) [ContinueDetail.java](https://gitee.com/jia-yan\_dong/code/blob/master/Java/javacode/chapter05/ContinueDetail.java)

*   基本介绍

    > 1. continue 语句用于结束本次循环，继续执行下一次循环
    > 2. continue 语句出现在多层嵌套的循环语句体中时，可以通过标签指明要跳过的是哪一层循环 , 这个和前面的标签的 使用的规则一样

### 3.return

[goto：Return01.java](https://gitee.com/jia-yan\_dong/code/blob/master/Java/javacode/chapter05/Return01.java)

*   基本介绍

    > 1. return 使用在方法，表示跳出所在的方法
    > 2. return后可以接返回值，表示该方法的返回值
