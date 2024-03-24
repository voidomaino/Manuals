
# bash 提示符

bash 的提示符由环境变量 PS1 (Prompt String 1) 描述。

默认的 bash 提示符包括：

* 用户名：`\u`
* 主机名：`\h`
* 当前工作目录：`\W`
* 提示符：`\$`

## git 分支

`__git_ps1` 函数由版本控制系统 git 提供，可以在提示符中显示分支信息。

```bash
export PS1='\u@\h \[\e[32m\]\w \[\e[91m\]$(__git_ps1)\[\e[00m\]$ '
```
