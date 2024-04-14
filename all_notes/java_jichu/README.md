# Java基础

## 1.Java 运行机制及运行过程&#x20;

> &#x20;语言的特点：跨平台性&#x20;
>
>
>
> ## <img src="../../.gitbook/assets/image (2).png" alt="" data-size="original">

## 2.Java核心机制-Java 虚拟机 \[JVM java virtual machine]&#x20;

1. 基本介绍

> 1. JVM 是一个虚拟的计算机，具有指令集并使用不同的存储区域。负责执行指令，管理数据、内存、寄存器，包含在 JDK 中
> 2. &#x20;对于不同的平台，有不同的虚拟机。
> 3. Java 虚拟机机制屏蔽了底层运行平台的差别，实现了“一次编译，到处运行”&#x20;

## 3.什么是 JDK、JRE&#x20;

* JDK 基本介绍

> 1. JDK 的全称(Java Development Kit Java 开发工具包) JDK = JRE + java 的开发工具 \[java, javac,javadoc,javap 等]
> 2. JDK 是提供给 Java 开发人员使用的，其中包含了 java 的开发工具，也包括了 JRE。所以安装了 JDK，就不用在单独 安装 JRE 了。

* JRE 基本介绍

> 1. JRE(Java Runtime Environment Java 运行环境) JRE = JVM + Java 的核心类库\[类]
> 2. 包括 Java 虚拟机(JVM Java Virtual Machine)和 Java 程序所需的核心类库等，如果想要运行一个开发好的 Java 程序， 计算机中只需要安装 JRE 即可。

* JDK、JRE 和 JVM 的包含关系

> 1. JDK = JRE + 开发工具集（例如 Javac,java 编译工具等)
> 2. JRE = JVM + Java SE 标准类库（java 核心类库）
> 3. 如果只想运行开发好的 .class 文件 只需要 JRE

## 4.Java代码规范

> 1. 类、方法的注释，要以javadoc的方式来写&#x20;
> 2. 非Java Doc的注释，往往是给代码的维护者看的，着重告述读者为什么这样写，如何修改，注意什么问题等
> 3. 运算符和=两边习惯性各加一个空格。比如：2 + 4 \* 5 + 345 - 89&#x20;
> 4. 源文件使用utf-8编码&#x20;
> 5. 行宽度不要超过80字符
> 6. 代码编写**次行风格**和**行尾风格（推荐使用）**

{% tabs %}
{% tab title="次行风格" %}
{% code lineNumbers="true" %}
```java
public class Demo
{
    public static void main(String[] args)
    {
        if(true)
        {
            System.out.println("true");
        }else
        {
            System.out.println("false");
        }
    }
}
```
{% endcode %}
{% endtab %}

{% tab title="行尾风格" %}
{% code lineNumbers="true" %}
```java
public class Demo{
    public static void main(String[] args){
        if(true){
            System.out.println("true");
        }else{
            System.out.println("false");
        }
    }
}
```
{% endcode %}
{% endtab %}
{% endtabs %}

