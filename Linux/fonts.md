# 字体

## 一些基本的概念

| 名称      | 衬线  | 等宽  | 语言      | 样式      | 表情支持  |
| -----     | ----- | ----- | -----     | -----     | -----     |
| Noto      | Sans  | mono  | Language  | Black     | nerd      |
| JetBrains | Serif |       |           | Bold      |           |
|           |       |       |           | Light     |           |
|           |       |       |           | Medium    |           |
|           |       |       |           | Regular   |           |
|           |       |       |           | Thin      |           |

serif 衬线字体，笔划末端带有笔锋，如宋体。

sans-serif 有时简称 sans 其中 sans 在法语中意为「没有」，即没有笔锋，如黑体。

monospace 有时简称 mono 意为等宽字体，便于代码对齐。

nerd font 有时简称 NF 表示表情（Unicode 字符）支持。

## 机制

### 安装

字体由 `fontconfig` 库管理。

文件 `/etc/fonts/font.conf` 定义字体文件`.ttf` 的保存位置。

```conf
<!-- Font directory list -->
        <dir>/usr/share/fonts</dir>
        <dir>/usr/share/X11/fonts/Type1</dir> <dir>/usr/share/X11/fonts/TTF</dir> <dir>/usr/local/share/fonts</dir>
        <dir prefix="xdg">fonts</dir>
        <!-- the following element will be removed in the future -->
        <dir>~/.fonts</dir>
```

用户自定义配置保存在文件 `/etc/fonts/local.conf` 中。

### 加载

`fc-cache [-v <dir_of_font>]`

### 查看

`fc-list [-v]`

标准输出中显示：

* 字体文件路径
* 字体族
* 字体样式

使用 `-v` 后缀显示更多内容。

## 应用

### i3wm

```txt
# .config/i3/config
font pango:<Font Family> [Other Options] <Size>
```
