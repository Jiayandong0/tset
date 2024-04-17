# 循环控制

## 1.for 循环控制

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

## 2.while 循环控制

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

## 3.do..while

g[oto：DoWhile01.java](https://gitee.com/jia-yan\_dong/code/blob/master/Java/javacode/chapter05/DoWhile01.java)

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


*
