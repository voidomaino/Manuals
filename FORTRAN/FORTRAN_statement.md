# 语句

更多有关的语句会在对应的章节解释，这里仅介绍一些基础的。

## 赋值语句

```BNF
<赋值语句> ::= <变量名称> = <算术表达式> | <字符表达式> | <逻辑表达式>
```

1. 进行数值型数据赋值的时候，要保持变量类型和表达式类型一致，否则会强制转变成变量的类型。
2. 进行字符型数据赋值的时候，多余的数据被舍弃，不足的补充空格；子串也可以作为变量名称进行赋值。
3. 进行逻辑型数据赋值的时候，`kind` 值以变量的 `kind` 值为准，改变储存的字节数，值不发生变换。

## PARAMETER

Fortran 规定用 `parameter` 语句来定义符号常量。

```BNF
<parameter 语句> ::= 
parameter"("<名称> = <表达式>{,<名称> = <表达式>}")"
```

1. 名称的作用域在整个程序单元；
2. 常量名需要在 `parameter` 语句前进行声明，否则遵循 I-N 规则；
3. 定义后的参数不能改变数值。

## 系统控制语句

### END

`end` 语句只能在主程序单元中使用，标志主程序单元结束，终止整个程序运行。

### STOP

`stop` 语句可以在主程序单元、模块单元、外部子程序中使用，用来随时终止程序运行，返回操作系统。

```BNF
<stop 语句> ::= stop[<整数>|<字符串>]
```

执行 `stop` 语句时输出整数或字符串，方便调试。

### PAUSE

`pause` 语句为暂停语句，能够暂停程序运行，按 `Enter` 键继续。

```BNF
<pause 语句> ::= pause[<整数>|<字符串>]
```

执行 `pause` 语句时输出整数或字符串，方便调试。