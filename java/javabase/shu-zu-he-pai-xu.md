# 数组和排序

[goto：**chapter06**](https://gitee.com/jia-yan\_dong/code/tree/master/Java/javacode/chapter06)

## 1.数组

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

## 2.排序

### 1.内部排序

*   介绍

    > 指将需要处理的所有数据都加载到内部存储器中进行排序。包括(交换式排序法、选择式排序法和插入式排序法)

### 2.外部排序法

*   介绍

    > 数据量过大，无法全部加载到内存中，需要借助外部存储进行排序。包括(合并排序法和直接合并排序法)

### 3.冒泡排序法

*   介绍&#x20;

    [goto:BubbleSort.java](https://gitee.com/jia-yan\_dong/code/blob/master/Java/javacode/chapter06/BubbleSort.java)

    > 冒泡排序（Bubble Sorting）的基本思想是：通过对待排序序列从后向前（从下标较大的元素开始），依次比较相邻元素 的值，若发现逆序则交换，使值较大的元素逐渐从前移向后部，就象水底下的气泡一样逐渐向上冒
*   代码示例

    {% code lineNumbers="true" %}
    ```java
    //使用冒泡排序法将其排成一个从大到小的有序数列
    int[] arr = {2,3,6,1,3};
    //临时变量
    int temp;
    for(int i = 0;i < arr.length;i++){
        for(int j = 0;j < arr.length - 1 - i;j++){
            if(arr[j] > arr[j + 1]){
                temp = arr[j];
                arr[j] = arr[j + 1];
                arr[j + 1] = temp;
            }
        }
    }
    ```
    {% endcode %}
