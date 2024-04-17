# 成员方法

## 1.成员方法

[goto：Method01.java](https://gitee.com/jia-yan\_dong/code/blob/master/Java/javacode/chapter07/Method01.java)

*   基本介绍

    > 在某些情况下，我们要需要定义成员方法(简称方法)。比如人类:除了有一些属性外( 年龄，姓名..),我们人类还有一 些行为比如:可以说话、跑步..,通过学习，还可以做算术题。这时就要用成员方法才能完成


*   方法的调用机制原理

    <figure><img src="../../../.gitbook/assets/image (4).png" alt=""><figcaption></figcaption></figure>


*   注意事项和使用细节

    [goto：MethodDetail.java](https://gitee.com/jia-yan\_dong/code/blob/master/Java/javacode/chapter07/MethodDetail.java)

    > * 访问修饰符 (作用是控制 方法使用的范围) 如果不写默认访问，
    >   1. \[有四种: public, protected, 默认, private], 具体在后面说
    > * 返回数据类型
    >   1. 一个方法最多有一个返回值 \[思考，如何返回多个结果 返回数组 ]
    >   2. 返回类型可以为任意类型，包含基本类型或引用类型(数组，对象)
    >   3. 如果方法要求有返回数据类型，则方法体中最后的执行语句必须为 return 值; 而且要求返回值类型必须和 return 的 值类型一致或兼容
    >   4. 如果方法是 void，则方法体中可以没有 return 语句，或者 只写 return ;
    > * 方法名&#x20;
    >   1. 遵循驼峰命名法，最好见名知义，表达出该功能的意思即可, 比如 得到两个数的和 getSum, 开发中按照规范

## 2.成员方法传参机制

### 1.基本数据类型的传参机制

[goto：MethodParameter01.java](https://gitee.com/jia-yan\_dong/code/blob/master/Java/javacode/chapter07/MethodParameter01.java)

*   结论

    > 基本数据类型，传递的是值（值拷贝），形参的任何改变不影响实参！

### 2.引用数据类型的传参机制

[goto：MethodParameter02.java](https://gitee.com/jia-yan\_dong/code/blob/master/Java/javacode/chapter07/MethodParameter02.java)

*   结论

    > 引用类型传递的是地址（传递也是值，但是值是地址），可以通过形参影响实参！

## 3.方法递归调用

*   基本介绍

    [goto：Recursion01.java](https://gitee.com/jia-yan\_dong/code/blob/master/Java/javacode/chapter07/Recursion01.java)

    > * 简单的说: 递归就是方法自己调用自己,每次调用时传入不同的变量.递归有助于编程者解决复杂问题,同时可以让代码变得简洁
    > *   内存解析图
    >
    >     <figure><img src="../../../.gitbook/assets/image.png" alt=""><figcaption></figcaption></figure>
*   递归重要规则

    > 1. 执行一个方法时，就创建一个新的受保护的独立空间（栈空间
    > 2. 方法的局部变量是独立的，不会相互影响，比如变量
    > 3. 如果方法中使用的是引用类型变量（比如数组，对象），就会共享该引用类型的数据&#x20;
    > 4. 递归必须向退出递归的条件逼近，否则就是无限递归，出现 StackOverflowError,死龟了：)&#x20;
    > 5. 当一个方法执行完毕，或者遇到return,就会返回，遵守谁调用，就将结果返回给谁，同时当方法执行完毕或者返回时，该方法也就执行完毕。


*   简单的案例

    [goto：RecursionExercise01.java](https://gitee.com/jia-yan\_dong/code/blob/master/Java/javacode/chapter07/RecursionExercise01.java)

    > * 猴子吃桃
    > * 斐波那契额数列
*   递归调用应用实例

    > * 迷宫 [goto：MiGong.java](https://gitee.com/jia-yan\_dong/code/blob/master/Java/javacode/chapter07/MiGong.java)
    > * 汉诺塔 [goto：HanoiTower.java](https://gitee.com/jia-yan\_dong/code/blob/master/Java/javacode/chapter07/HanoiTower.java)

## 4.方法重载

