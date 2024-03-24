# 百度网盘

[Baidupcs](https://github.com/qjfoidnh/BaiduPCS-Go) 过于好用，不得不记下来。
在 `$HOME/.local/share/applications` 目录下创建 `baidunetdisk.desktop` 文件，内容如下：

```txt
[Desktop Entry]
Version = 1.0
Name = Baidu Netdisk
Type = Application
Comment = 百度网盘命令行客户端
Path = /bin
Exec = alacritty -e baidupcs %F
Terminal = false
Categories = Network;
```
