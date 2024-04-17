# 对象创建的流程分析

*   看一个案例

    > 1. {% code lineNumbers="true" %}
    >    ```java
    >    public class Person{
    >       int age = 90;
    >       String name;
    >       Person(String n,int a){
    >          age = a;
    >          name = n;
    >       }
    >       public static void main(String[] args){
    >          Person person = new Person("jack",20);
    >       }
    >    }
    >    ```
    >    {% endcode %}
    > 2. 流程分析
    >
    > > 1. 加载Person类信息(Person.class),只会加载一次
    > > 2. 在堆中分配空间地址
    > > 3. 完成对象初始化
    > >    1. 默认初始化age=0name=nul
    > >    2. 显式初始化 age90,name≡null,
    > >    3. 构造器的初始化age=20,name=jack]
    > > 4. 在对象在堆中的地址，返回给p(P是对象名，也可以理解成是对象的引用)
