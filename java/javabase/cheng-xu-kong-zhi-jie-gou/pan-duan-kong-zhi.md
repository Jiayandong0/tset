# 判断控制

## 1.顺序控制

*   基本介绍

    > 程序从上到下逐行地执行，中间没有任何判断和跳转


*   流程图

    <figure><img src="../../../.gitbook/assets/image (5).png" alt="" width="219"><figcaption></figcaption></figure>



## 2.分支控制 if-else

### 1.单分支

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

    <figure><img src="../../../.gitbook/assets/image (1) (1).png" alt=""><figcaption></figcaption></figure>

### 2.双分支

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

    <figure><img src="../../../.gitbook/assets/image (2) (1).png" alt="" width="477"><figcaption></figcaption></figure>

### 3.多分支

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

    <figure><img src="../../../.gitbook/assets/image (4) (1).png" alt="" width="563"><figcaption></figcaption></figure>

### 4.嵌套分支

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

## 3.switch 分支结构

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

    <figure><img src="../../../.gitbook/assets/image (5) (1).png" alt="" width="563"><figcaption></figcaption></figure>


*   注意事项和细节讨论  [goto：SwitchDetail.java](https://gitee.com/jia-yan\_dong/code/blob/master/Java/javacode/chapter05/SwitchDetail.java)

    > 1. 表达式数据类型，应和case后的常量类型一致，或者是可以自动转成可以相互比较的类型，比如输入的是字符，而常量是int&#x20;
    > 2. switch(表达式)中表达式的返回值必须是：(byte、short、int、char、enum\[枚举]，String)
    > 3. case子句中的值必须是常量，而不能是变量&#x20;
    > 4. default子句是可选的，当没有匹配的case时，执行default&#x20;
    > 5. break语句用来在执行完一个case分支后使程序跳出switch语句块；如果没有写 break,程序会顺序执行到switch结尾，除非遇到break;


*   switch 和 if 的比较

    > 1. 如果判断的具体数值不多，而且符合 byte、 short 、int、 char, enum\[枚举], String 这 6 种类型。虽然两个语句都可 以使用，建议使用 swtich 语句
    > 2. 其他情况：对区间判断，对结果为 boolean 类型判断，使用 if，if 的使用范围更广
