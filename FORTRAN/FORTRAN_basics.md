# Fortran 95 基础知识

## 字符集

构成 Fortran 95 程序的基本字符表示为

```BNF
<字符> ::= <英文字母> | <阿拉伯数字> | "_" | <特殊字符>
<英文字母> ::= <大写字母> | <小写字母>
<大写字母> ::= A | B | C | ...
<小写字母> ::= a | b | c | ...
<阿拉伯数字> ::= 0 | 1 | 2 | ...
<特殊字符> ::= = | + | - | * | / | ( | ) | , | . | ' | : | ! | " | % | & | ; | < | > | ? | $ | " " 
```

Fortran 95 程序不区分大小写，字符串中的字符除外；其他字符只允许出现在注释、字符串、输入输出数据中。

## 名称

名称用来定义实体（变量、命名常量、函数、过程、程序单元、公用块、派生类型、结构体、数组和哑元）。

```BNF
<名称> ::= <英文字母>{<英文字母>|<数字>|"_"}
```

名称不可超过 31 个字符。

名称有一定的作用域，即适用范围。名称作用域为该名称声明所在的程序单元、函数或过程。在作用域外的名称需要重新定义。作用于整个程序的名称为**全局名称**，否则为**局部名称**。一个名称要么全局，要么局部。

## 关键字

Fortran 95 中有一些特殊的名称，用来描述语句语法成分或命名哑元，被称为关键字。

**语句关键字**描述语句语法成分，如 `if`、`then`、`program` 等。

**变元关键字**命名哑元，如 `vecter`、`mask`、`field` 等。

关键字有特定的含义，在程序中有具体的位置要求，胡乱改变将产生语法错误。

Fortran 95 中的关键字可以作为其他实体存在，但为了提高可读性，应当避免这样的情况发生。

## 程序结构

```BNF
<程序> ::= <主程序单元>{<外部子程序单元> | <模块单元> | <数据块单元>}
<主程序单元> ::=
 [<program 语句>]
 [<说明部分>]
 [<操作部分>]
 [<内部子程序部分>]
 <end 语句>
<program 语句> ::= program <程序名称>
<说明部分> ::=
 {<内部数据类型说明语句>
 |<派生数据类型说明语句>
 |<数组类型说明语句>
 |<指针类型说明语句>}
<操作部分> ::= {<可执行语句>}
<内部子程序部分> ::= 
 contains
 {<内部子程序>}
<end 语句> ::= end [program [<程序名称>]]
<程序名称> ::= <名称>
```

`<外部子程序单元>` 是由不包含在主程序单元、模块单元和其他外部子程序单元中的函数或子例行程序所构建的程序单元，能够被其他程序单元调用执行。外部子程序单元以 `function` 或 `subroutine` 语句开头。

`<模块单元>` 是能够被其他程序单元访问的一组定义（数据实体定义、数据类型定义、过程定义、过程接口定义）所构成的程序单元。其中过程定义又称为模块子程序，允许被模块中其他模块子程序访问。模块单元以 `module` 语句开头。

`<数据块单元>` 是命名公用区中变量指定初始值的程序单元，不可被执行。数据块单元以 `block data` 语句开头。

如果没有出现 `<program 语句>`，将指定 `main$"文件名"` 为主程序名称。程序名称一旦指定，则为全局名称。

## 语句

语句可以说是程序的主体了。**可执行语句**表示程序要完成的某个操作；**非可执行语句**描述程序的某种属性（数据的特性、编辑、转换等信息）。

语句要求按规定次序排列。以下语句次序由先往后排列：

1. `option`
2. `program` `function` `subroutine` `module` `block data`
3. `use`
4. `implicit none` `namelist` `format` `entry`
5. `parameter` `lmplicit` `namelist` `format` `entry`
6. `parameter` `data` `namelist` `format` `entry` 其他定义、说明类语句
7. `data` `namelist` `format` `entry` 可执行语句
8. `contains`
9. 内部子程序或模块子程序
10. `end`

注释行，`include` 可以插入在 `end` 之前的所有行内。

在程序单元内有的语句是不能使用的。

## 程序编辑格式

不同的书面格式的 Fortran 文件带有不同的后缀名。

* 在固定格式下，Fortran 文件名为

``` fortran
*.f
*.for
```

* 在自由格式下，Fortran 文件名为

``` fortran
*.f90
```

Fortran 95 采用**自由格式**，放弃了原有的固定格式。自由格式的特征为：

1. 语句在一行中的位置不受限制，长度可达 132 个字符；
2. 空格被限制使用，只能出现在两个关键字、名称、常量、标号之间，或者字符串文本之中；
3. 注释标志符 `!` 允许出现在任意位置。在第一列，则该行为注释；不在第一列，则该行之后为注释；
4. 一行允许多个语句，用 `;` 分割，最后一句末尾不能带有 `;`；
5. 续行标志符 `&` 允许出现在待续行语句的末尾，其下第一个非注释行为续行，最多可以由 39 个续行。单词内续行，需要在续行行首加上续行标志符 `&`。