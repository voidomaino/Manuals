# CASE

`case` 选择语句类似多分支选择结构，
能够根据表达式的计算结果，从多个分支中选择一个执行。

```fortran
SELECT CASE (<表达式 E>)
CASE (<控制集合 1>)
    <语句 1>
CASE (<控制集合 2>)
    <语句 2>
...
CASE (<控制集合 N>)
    <语句 N>
CASE DEFAULT
    <语句 N+1>
END SELECT
```

其中表达式的值可以是整型、字符型和逻辑型。

控制集合中列出了要执行对应语句表达式的值的所有可能，如

```fortran
1,5,7:9
'pen', 'pencil', 'desk'
.TRUE.
```
两个不同的控制集合不能有相同的元素。

