
# CYCLE

`CYCLE` 语句的功能是，在循环执行过程中强制终止本次循环语句的执行，
跳转到 `DO` 后的第一句。

示例：

```fortran
DO i=2,5
    PRINT "(1X,I3)", I
    IF (I>3) CYCLE
    PRINT "(1X,I3)", I
ENDDO
```

结果为：

```text
2
2
3
3
4
5
```
