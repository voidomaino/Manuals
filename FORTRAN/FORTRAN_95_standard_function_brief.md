# FORTRAN 90 标准函数简表

符号约定：

1. `I` 代表整型；`R` 代表实型；`C` 代表复型；`CH` 代表字符型；`S` 代表字符串；`L` 代表逻辑型；`A` 代表数组；`P` 代表指针；`T` 代表派生类型；`AT` 为任意类型。
2. `s:P` 表示变元 s 为 P 类型（任意 kind 值）。`s:P(k)` 表示变元 s 为 P 类型（kind=k）。
3. `…` 表示可选参数。
4. `*` 表示常用函数。

## 数值和类型转换函数

输出的结果类型一般向输入类型看齐，除非

| **函数名**           | **说明**                                                     | 输入类型        | 输出类型        |
| -------------------- | ------------------------------------------------------------ | --------------- | --------------- |
| ABS(x)*              | 求 $x$ 的绝对值 $\abs{x}$。                                  | I<br />R<br />C | I<br />R<br />R |
| AIMAG(x)             | 求 $x$ 的实部。                                              | C               | R               |
| AINT(x[,kind])*      | 对 $x$ 取整，并转换为实数（kind）。 $x$ :R， kind:I， 结果:R（kind） | R               |                 |
| AMAX0(x1,x2,x3,…)*   | 求x1、x2、x3、…中最大值。xI:I， 结果:R                       |                 |                 |
| AMIN0(x1,x2,x3,…)*   | 求x1,x2,x3,…中最小值。xI:I, 结果:R                           |                 |                 |
| ANINT(x[,kind])*     | 对x四舍五入取整,并转换为实数（kind）。x:R, kind:I, 结果:R（kind） |                 |                 |
| CEILING(x)*          | 求大于等于x的最小整数。x:R, 结果:I                           |                 |                 |
| CMPLX(x[,y][,kind])) | 将参数转换为x、（x,0.0）或（x,y）。x:I、R、C, y:I、R,kind:I, 结果:C（kind） |                 |                 |
| CONJG(x)             | 求x的共轭复数。x:C, 结果:C                                   |                 |                 |
| DBLE(x)*             | 将x转换为双精度实数。x:I、R、C, 结果:R（8）                  |                 |                 |
| DCMPLX(x[,y])        | 将参数转换为x、（x,0.0）或（x,y）。x:I、R、C, y:I、R, 结果:C（8） |                 |                 |
| DFLOAT(x)            | 将x转换为双精度实数。x:I, 结果:R（8）                        |                 |                 |
| DIM(x,y)*            | 求x-y和0中最大值, 即MAX（x-y,0）。x:I、R, y的类型同x,结果类型同x |                 |                 |
| DPROD(x,y)           | 求x和y的乘积,并转换为双精度实数。x:R, y:R, 结果:R（8）       |                 |                 |
| FLOAT(x)*            | 将x转换为单精度实数。x:I, 结果:R                             |                 |                 |
| FLOOR(x)*            | 求小于等于x的最大整数。x:R, 结果:I                           |                 |                 |
| IFIX(x)*             | 将x转换为整数（取整）。x:R, 结果:I                           |                 |                 |
| IMAG(x)              | 同AIMAG（x）                                                 |                 |                 |
| INT(x[,kind])*       | 将x转换为整数（取整）。x:I、R、C, kind:I, 结果:I（kind）     |                 |                 |
| LOGICAL(x[,kind])*   | 按kind值转换新逻辑值。x:L, 结果:L（kind）                    |                 |                 |
| MAX(x1,x2,x3,…)*     | 求x1,x2,x3,…中最大值。xI为任意类型, 结果类型同xI             |                 |                 |
| MAX1(x1,x2,x3,…)*    | 求x1,x2,x3,…中最大值（取整）。xI:R, 结果:I                   |                 |                 |
| MIN(x1,x2,x3,…)*     | 求x1,x2,x3,…中最小值。xI为任意类型, 结果类型同xI             |                 |                 |
| MIN1(x1,x2,x3,…)*    | 求x1,x2,x3…中最小值（取整）。xI:R, 结果:I                    |                 |                 |
| MOD(x,y)*            | 求x/y的余数,值为x-INT（x/y）*y。x:I、R, y的类型同x, 结果类型同x |                 |                 |
| MODULO(x,y)          | 求x/y余数,值为x-FLOOR（x/y）*y。x:I、R, y的类型同x, 结果类型同x |                 |                 |
| NINT(x[,kind])*      | 将x转换为整数（四舍五入）。x:R, kind:I, 结果:I（kind）       |                 |                 |
| REAL(x[,kind])*      | 将x转换为实数。x:I、R、C, kind:I, 结果:R（kind）             |                 |                 |
| SIGN(x,y)*           | 求x的绝对值乘以y的符号。x:I、R, y的类型同x, 结果类型同x      |                 |                 |
| SNGL(x)              | 将双精度实数转换为单精度实数。x:R（8）, 结果:R               |                 |                 |
| ZEXT(x)              | 用0向左侧扩展x。x:I、L, 结果:I                               |                 |                 |