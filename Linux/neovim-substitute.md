
# VIM 查找并替换

`:substitute` 命令查找并替换文本，基础用法：

```command
:<范围>s/<查找表达式>/<替换表达式>/<选项>
```

## 范围

`%` 表示对全部文件执行。
`5,12` 表示对第 5 到第 12 行执行。
`'a,'b` 表示对标记 a 到标记 b 之间的内容执行。
`'<,'>` 表示对视觉模式下的选中每一行执行。
`.,$` 表示对当前行到末尾之间的内容执行。
`.,+2` 表示对当前行和后两行中的内容执行。
`g/^bar/` 表示对所有以 `bar` 开头的行执行。

## 选项

`g` 表示对整行执行（没有声明则只对第一个执行）；  
`c` 表示每次执行时进行确认；
`i` 表示查找时不考虑大小写；
`I` 表示查找时考虑大小写。

## 查找表达式

`\<foo\>` 表示查找 **单词** `foo`；
`foo\C` 表示查找文本 `foo` 不考虑大小写。
`\t` 表示 tab；
`\s` 表示空格和多个空格或 tab；
`\n` 表示新的一行；
`\r` 表示回车；
`[0-9]` 表示数字 0 到 9；
`foo.\{2}` 表示查找 `foo.` 并选中后面的两个字符；
`foo \zs2017\ze bar` 表示查找 `foo 2017 bar` 但是替换内容只有 `2017`

## 替换表达式

`\r` 表示新的一行，`\n` 不再生效；
`&` 表示查找表达式匹配的内容
