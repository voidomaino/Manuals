# 数组

对涉及大量数据的处理，使用数组可以使程序变得简洁灵活。

数组是类型相同的一组变量的有序集合，任何一组类型相同且有序的变量都可以定义成数组。

## 声明

在程序中使用数组，必须先进行声明。

### 显式声明

```BNF
<数组声明语句> ::= 
<类型声明符> [::] <数组声明表>

<类型声明符> ::= 
INTEGER | REAL | COMPLEX | CHARACTER | LOGICAL

<数组声明表> ::= 
<数组名>(<维说明表>)[=<数组初值>]{, <数组名>(<维说明表>)[=<数组初值>]}

<维说明表> ::= 
<维说明符>{,<维说明符>}

<维说明符> ::= 
[<下界>:]<上界>

<数组初值> ::= <数组构造器>
```

`<类型声明符>` 后可以声明 `kind` 值。

`::` 用于给数组赋初值。

`<维说明表>` 指定数组的维数，`<维说明符>` 指定数组的上、下界，下界缺省为 1。上下界都为整数，步长只能是 1（省略），上下界相等，则数组大小为 0，元素个数为 1。

**数组构造器**

数组构造器是指按数组 *存储结构* 次序排列的，又一系列数值或隐含 DO 循环组成的一个线性表，线性表放在圆括号和斜杠之间。通常使用数组构造器来对数组进行赋初值。

```BNF
<数组构造器> ::=
(/<数组初值表>/)

<数组初值表> ::=
<初值项>{,<初值项>}

<初值项> ::=
<初值>|<隐含 DO 循环>
```

使用隐含 DO 循环时，只能给以为数组赋值。对于多维数组，需要使用 RESHAPE 函数。

**SHAPE**

数组的维数和下标上下界，统称为数组的形（SHAPE）。

### DIMENSION

DIMENSION 语句也可用于声明数组，和显式声明的区别为，数组类型由 I-N 规则决定，并且 DIMENSION 语句不能对数组赋初值。

```BNF
<DIMENSION 语句> ::= 
DIMENSION <数组声明表>
```

在 DIMENSION 语句前对变量进行类型声明，可以改变 I-N 规则的适用范围。

### 合二为一

前面两种声明方式合二为一，描述为：

```BNF
<带 DIMENSION 的类型声明语句> ::=
<类型声明符>,DIMENSION"(" <维说明表> ")" :: <数组声明表>
```

适合对具有相同维数和上下界的多个数组进行声明，维数和上下界由 DIMENSION 语块决定，当然也可随后在数组名称之后修改定义。

不能省略 `::` ，可以赋初值。

## 引用

```BNF
<数组元素引用> ::=
<数组名>[(<数组下标>{,<数组下标>})]

<数组下标> ::=
<表达式>|<下界表达式>:<上界表达式>:<步长>
```

只给出数组名不给出数组下标，则表示全部数组元素。

下标为整型或实型表达式，实型自动取整。

使用 `<下界表达式>:<上界表达式>:<步长>` 的方式可按间隔同时引用多个数组元素。

下标应在上下界之间，否则会产生错误。

## 存储结构和逻辑结构

存储时，数组连续排列，先变动第一位，再变动第二位。

`integer a(-5:8,-3:4,10:15)` 总共有 672 个元素，其中 `a(2,1,13)` 是第 400 个。

逻辑结构是显然的。对于二维数组，`(行,列)`。

## 输入和输出

数组可以通过数据的格式化输入输出函数被引用输出，使用循环表达可以轻松达到。

和普通的输入输出不一样的是，数组的输入输出可以通过隐含 DO 循环子句的方式输入输出，达到简化表达的效果。

对于一维数组，隐含 DO 循环子句的一般格式为：

```BNF
<隐含 DO 循环> ::=
(<循环项>,<循环变量>=<初值>,<终值>[,<步长>])
```

例如

```fortran
read *, (score(i),i=1,n,2)
```

对于二维数组，隐含 DO 循环子句的一般格式为：

```BNF
<隐含 DO 循环> ::=
((<循环项>,<循环变量 1>=<初值 1>,<终值 1>[,<步长 1>]),<循环变量 2>=<初值 2>,<终值 2>[,<步长 2>])
```

例如

```fortran
read *, ((a(i,j),j=1,n),i=1,m)
```

## 数组函数

### UBOUND/LBOUND

这两个函数可以检测数组的下标上下界。以 UBOUND 为例：

```BNF
<UBOUND 调用>  ::=
UBOUND (<数组名>[,[DIM=]<整型表达式>])
```

`<整型表达式>` 用于确定数组的第几维，函数返回一个整型值，表示对应维的上界；

若没有 `<整型表达式>` ，则函数返回一个数组，依次表示对应维的上界。

使用这个函数可以检测引用数组的值不至于偏离数组下标的上下界。

### DATA

DATA 语句也称为赋初值语句， DATA 语句可以按 *存储结构* 给普通变量、整个数组、数组片段、单一数组元素、结构体、结构体成员赋初值。

```BNF
<DATA 语句> ::=
DATA<对象表>/<初值表>/{,<对象表>/<初值表>/}

<对象表>::=
<变量>|<数组>|<数组片段>|<数组元素>|<结构体>|<隐含 DO 循环>

<初值表>::=
<初值项>{,<初值项>}

<初值项>::=
<初值>|<重复系数>*<初值>
```

初值只能是常量，不能是变量、数组元素或其他表达式。

### WHERE

WHERE 语句用于判定并处理数组元素，有三种格式。

**逻辑 WHERE 语句**

```BNF
<逻辑 WHERE 语句>::=
WHERE(<关系/逻辑表达式>)<赋值语句>
```

在 `关系/逻辑表达式` 中引用数组名称而不带下标，表示依次引用数组的每个元素，当该元素满足表达式的条件，即逻辑值为真时，运行赋值语句。

在 `关系/逻辑表达式` 中可以存在两个数组名称，要求是两个数组的维说明相同。引用时，对应下标也相同。

**块 WHERE 语句**

```BNF
<块 WHERE 语句>::=
WHERE(<关系/逻辑表达式>)
  <赋值语句 1>
[ELSEWHERE
  <赋值语句 2>]
END WHERE
```

**多分支 WHERE 语句**

```BNF
<多分支 WHERE 语句>::=
WHERE(<关系/逻辑表达式>)
  <赋值语句 1>
ELSEWHERE(<条件 2>)
  <赋值语句 2>
ELSEWHERE(<条件 3>)
  <赋值语句 3>
ELSEWHERE(<条件 4>)
  <赋值语句 4>
...
ELSEWHERE(<条件 n>)
  <赋值语句 n>
ELSEWHERE
  <赋值语句 n+1>
END WHERE
```

### FORALL

FORALL 语句又称为并行处理语句，能够实现对一个数组的所有元素同时进行赋值或运算。

**逻辑 FORALL 语句**

```BNF
<逻辑 FORALL 语句>::=
FORALL (<三项说明>{,<三项说明>}[,<条件>])<赋值语句>

<三项说明>::=
<变量>=<表达式 1>:<表达式 2>[:<表达式 3>]
```

变量指代数组下标，必须为整型。

三个表达式分别指代数组的某维下界、上界、步长。

条件对数组元素进行筛选，通过后再执行后面的赋值语句。

**块 FORALL 语句**

```BNF
<块 FORALL 语句>::=
FORALL (<三项说明>{,<三项说明>}[,<条件>])
  {<FORALL 体语句>}
END FORALL

<FORALL 体语句>::=
<数组赋值语句>|<指针赋值语句>|<WHERE 语句>|<FORALL 语句>
```

## 动态数组

对 SHAPE 不确定的数组，可以使用动态数组来避免声明时使用巨大的数组范围，节约存储空间。

### 声明

```BNF
<动态数组声明语句>::=
<类型声明符>, DIMENSION(:{,:}), ALLOCATABLE :: <数组名表>

<数组名表>::=
<数组名>(:{,:}){，<数组名>(:{,:})}
```

声明中不指定数组的上界和下界，数组实际上并不存在，还需要使用 ALLOCATE 语句重新定义一下数组。

**ALLOCATE**

```BNF
<ALLOCATE 语句>::=
ALLOCATE(<动态数组声明表>[,STAT=<状态变量>])

<动态数组声明表>::=
<数组名>(<维说明表>){,<数组名>(<维说明表>)}
```

当 ALLOCATE 语句中的数组与声明中的数组维数不一致时，数组是无法定义的。STAT 值用来检测这一情况，成功定义，则状态变量将被赋值为 0；若定义不成功，状态将被定义为错误符号。ALLOCATE 语句中没有指定状态变量时，定义失败将造成系统报错，强制结束。

声明过程中不能同时对数组进行赋值。

### 删除

当动态数组不再使用，需及时通过 DEALLOCATE 语句释放存储空间。

```BNF
<DEALLOCATE 语句>::=
DEALLOCATE(<数组表>[,STAT=<状态参量>])
```




