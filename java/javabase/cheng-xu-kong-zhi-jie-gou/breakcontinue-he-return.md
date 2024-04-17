# break、continue和return

## 1.break

[goto：Break01.java](https://gitee.com/jia-yan\_dong/code/blob/master/Java/javacode/chapter05/Break01.java)

*   基本介绍

    > break 语句用于终止某个语句块的执行，一般使用在 switch 或者循环\[for , while , do-while]中


*   细节 [goto：BreakDetail.java](https://gitee.com/jia-yan\_dong/code/blob/master/Java/javacode/chapter05/BreakDetail.java)

    > 1. break语句可以指定退出哪层&#x20;
    > 2. label1是标签，名字由程序员指定
    > 3. break后指定到哪个label就退出到哪里
    > 4. 在实际的开发中，尽量不要使用标签
    > 5. 如果没有指定break，默认退出最近的循环体

## 2.continue

goto：[Continue01.java](https://gitee.com/jia-yan\_dong/code/blob/master/Java/javacode/chapter05/Continue01.java) [ContinueDetail.java](https://gitee.com/jia-yan\_dong/code/blob/master/Java/javacode/chapter05/ContinueDetail.java)

*   基本介绍

    > 1. continue 语句用于结束本次循环，继续执行下一次循环
    > 2. continue 语句出现在多层嵌套的循环语句体中时，可以通过标签指明要跳过的是哪一层循环 , 这个和前面的标签的 使用的规则一样

## 3.return

[goto：Return01.java](https://gitee.com/jia-yan\_dong/code/blob/master/Java/javacode/chapter05/Return01.java)

*   基本介绍

    > 1. return 使用在方法，表示跳出所在的方法
    > 2. return后可以接返回值，表示该方法的返回值


*
