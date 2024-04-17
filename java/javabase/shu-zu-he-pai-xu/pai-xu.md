# 排序

## 1.排序的分类

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
