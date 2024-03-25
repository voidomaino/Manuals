
# PARAMETER

FORTRAN 规定用 `PARAMETER` 语句来定义符号常量。

```fortran
PARAMETER (<名称> = <表达式>{,<名称> = <表达式>})
```

1. 名称的作用域在整个程序单元；
2. 常量名需要在 `PARAMETER` 语句前进行声明，否则遵循 I-N 规则；
3. 定义后的参数不能改变数值。
