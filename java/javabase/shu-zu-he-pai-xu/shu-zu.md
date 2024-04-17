# 数组

## 1.数组的使用

*   基本介绍

    [goto：Array01.java](https://gitee.com/jia-yan\_dong/code/blob/master/Java/javacode/chapter06/Array01.java)

    > 数组可以存放多个同一类型的数据。数组也是一种数据类型，是引用类型。 即：数(数据)组(一组)就是一组数据


*   使用

    [goto：Array02.java](https://gitee.com/jia-yan\_dong/code/blob/master/Java/javacode/chapter06/Array02.java)

    *   方式一-动态初始化

        > int a\[]  = new int \[5];


    *   方式二-静态初始化

        > int a\[]  = {1,2,3,4,5};


*   数组使用注意事项和细节

    [goto：ArrayDetail.j ava](https://gitee.com/jia-yan\_dong/code/blob/master/Java/javacode/chapter06/ArrayDetail.java)

    > 1. 数组是多个相同类型数据的组合，实现对这些数据的统一管理
    > 2. 数组中的元素可以是任何数据类型，包括基本类型和引用类型，但是不能混用
    > 3. &#x20;数组创建后，如果没有赋值，有默认值 int 0，short 0, byte 0, long 0, float 0.0,double 0.0，char \u0000，boolean false，String null
    > 4. 使用数组的步骤 1. 声明数组并开辟空间 2 给数组各个元素赋值 3 使用数组
    > 5. 数组的下标是从 0 开始的
    > 6. 数组下标必须在指定范围内使用，否则报：下标越界异常
    > 7. 数组属引用类型，数组型数据是对象(object)
