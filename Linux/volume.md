
# 音量控制

`alsa` 是内核的发声部分，只要发出声音就少不了。
这部分是 Linux 系统内置的，不需要安装。

`pulseaudio` `jack` `pipewire` 是三个品牌的混成器，负责把不同来源的声音混合在一起。

这里只讲解 `pipewire`，因为 `pipewire` 能够做到兼顾其它的各种混成器。

安装 `pipewire`。

安装 `pipewire-jack` 因为 `ffmpeg` 要用。

安装 `pipewire-pulse` 来管理音量。
没错 `pipewire` 本身不能管理音量，还要借助 `pulseaudio`。

安装 `pipewire-alsa` 来沟通内核。

安装 `wireplumber` 来统领各种混成器。

在用户层面使用 `systemd` 启动服务进程：

```bash
systemctl --user --now enable pipewire pipewire-pulse wireplumber
```

看起来装三个，实际上都由 `pipewire` 管理。
这样总比装了 `pulseaudio` 又装 `jack2` 好。

通过 `pactl` 管理音量，`pavucontrol` 图形界面管理音量。

对于 i3 桌面环境，可以用 `github` 上的 `i3-volume` 设置键盘快捷键。
