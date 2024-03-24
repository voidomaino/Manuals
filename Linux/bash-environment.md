# Shell 环境

Shell 在 shell 会话中保存着大量信息，这些信息被称为环境。
程序获取环境中的数据（即环境变量）来了解本机的配置。

使用命令 `printenv` 来查看环境变量。

`.profile`：在每次登录，并进入 Bourne Shell 后读取；

`.bash_profile`：在每次登录，并进入 bash 后读取，
如果没有此文件，由 `.profile` 取代；

`.bashrc`：在每次打开交互终端时读取，在 Shell 脚本里不读取；

`.xinitrc`：以 `startx` 程序启动 `X` 服务时读取；
用于保存 `startx` 的有关配置，如启动某个桌面环境。

`.xprofile`：在启动桌面管理器之前读取；
用于设置某些开机后就一直要起作用的变量和开机自启的某些程序。

## PATH 变量

每个变量的实质都是一个字符串。在 shell 中字符串可以通过定义来延长。

```shell
PATH=$HOME/bin:$PATH
```

使用 `export` 命令使得 shell 子进程可以使用修改后的 `PATH` 变量。
