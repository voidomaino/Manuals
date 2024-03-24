
# 文件类型插件

## 什么是插件？

插件就是在启动 `vim` 时被加载的 `vimscript` 或 `lua` 文件。

## 插件是怎么被加载的？

`vim` 的 `runtimepath` 变量是一系列的目录，当 `vim` 启动时，它从这些目录下寻找
需要加载的文件。运行命令 `:echo &runtimepath` 来查看当前 `runtimepath` 的值。

`runtimepath` 下可能有这么一些文件和目录，此处列举其结构。

| 文件或目录的名称  | 描述      |
| -----             | -----     |
| `filetype.vim`    | 设置文件的 `filetype` 值                  |
| `autoload/`       | 由 `vim` 的 `autoload` 特性决定是否加载   |
| `colors/`         | `vim` 的配色方案                          |
| `doc/`            | 包含文档和帮助                            |
| `plugin/`         | 全局插件                                  |
| `ftplugin/`       | 与文件类型有关的插件                      |
| `pack/`           | 第三方插件的默认位置                      |
| `syntax/`         | 与语法高亮有关的插件                      |

`plugin/` 和 `ftplugin/` 下插件的区别：

* `plugin/` 中的文件在 `ftplugin/` 前加载；
* `plugin/` 中的文件在一个 `vim` 进程中只运行一次，而 `ftplugin/` 中的文件每打
  开一个 `buffer` 就加载一次。

## `ftplugin` 系统的运作

### 打开 `ftplugin` 功能

`neovim` 默认打开文件类型功能。

### 识别文件的 `filetype` 值

一般而言，`neovim` 会自动识别，但是可以在 `&runtimepath/filetype.vim` 中处定义
识别方法。

不同的文件类型有各自的 `filetype` 值，`LaTeX` 文件的值为 `tex`，`.py` 文件的值为
`python`，`Lua` 文件的值为 `lua`。

### `<filetype>.vim` 发挥作用

当打开一个 `LaTeX` 文件时，`ftplugin/tex.vim` 文件中的设置就有效了。



