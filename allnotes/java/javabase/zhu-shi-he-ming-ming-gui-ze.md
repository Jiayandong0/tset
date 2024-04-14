# 注释和命名规则

## 1.文档注释

* 说明

> 注释内容可以被JDK提供的工具javadoc所解析，生成一套以网页文件形式体现的该程序的说明文档，一般写在类

* 基本使用

```sh
javadoc -d 文件夹名 -author -version Demo.java
```

## 2.标识符命名规范

> 1. 包名：多单词组成时所有字母都小写：aaa.bbb.ccc //比如 com.hsp.crm
> 2. 类名、接口名：多单词组成时，所有单词的首字母大写：XxxYyyZzz \[大驼峰] 比如： TankShotGame
> 3. 变量名、方法名：多单词组成时，第一个单词首字母小写，第二个单词开始每个单词首字母大写：xxxYyyZzz \[小 驼峰， 简称 驼峰法] 比如： tankShotGame
> 4. 常量名：所有字母都大写。多单词时每个单词用下划线连接：XXX\_YYY\_ZZZ 比如 ：定义一个所得税率 TAX\_RATE
