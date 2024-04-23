
# INTEGER

显式声明整型变量、数组：

```fortran
INTEGER(KIND=2) a,b,c,d     
INTEGER(1) e,f,g            
INTEGER f                   
INTEGER(KIND=2) :: a=15, b  
INTEGER(1) :: c=8#127
INTEGER :: d=125

INTEGER(KIND=2) array(1:2,3:4,6)    ! 数组的下界缺省为 1
INTEGER array2(1:1,3:4,6)    ! 上下界相等，则数组大小为 0，元素个数为 1
```

如果要声明无符号整型量，用 `UNSIGNED` 取代 `INTEGER`，建议少用。
