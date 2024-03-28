
# INTEGER

显式声明整型变量：

```fortran
INTEGER(KIND=2) a,b,c,d     ! 括号可以用 * 取代：INTEGER*2 a,b,c,d；推荐使用
INTEGER(1) e,f,g            ! 当 KIND=1 时可以用 BYTE 取代：BYTE e,f,g
INTEGER f                   ! 不指定整型 KIND 值则默认为 4；
INTEGER(KIND=2) :: a=15, b  ! 仅当 :: 存在时整型变量可以在声明时赋初值。
INTEGER(1) :: c=8#127
INTEGER :: d=125
```

如果要声明无符号整型量，用 `UNSIGNED` 取代 `INTEGER`，建议少用。
