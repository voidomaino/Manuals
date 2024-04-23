# IMPLICIT

I-N 规则规定：变量名以字母 `I J K L M N I J K L M N`
为开头的变量默认为整型变量，其他为实型变量。

`IMPLICIT` 隐式声明语句可以重新定义 I-N 规则。

`IMPLICIT` 语句语法描述如下：

```fortran
IMPLICIT NONE               ! 取消 I-N 规则
IMPLICIT INTEGER(q,w,e,r,t) ! 以规则：q、w、e、r 和 t 开头的变量为整型替代 I-N 规则
IMPLICIT REAL(x-z)          ! 以规则：x、y 和 z 开头的变量为实型替代 I-N 规则
```

同一个字母不能被 `IMPLICIT` 语句提及两次； `,` 表示枚举； `-` 表示按顺序批量指定。

类型声明语句可覆盖 `IMPLICIT` 语句。
