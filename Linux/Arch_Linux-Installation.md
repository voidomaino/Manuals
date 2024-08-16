
# Arch Linux Installation

## Before Installation

- Make a Installation Media.

## Basic System Installation

- Enter the `root@archiso`
- Disable and stop `reflector.service`
- Use `iwctl` to connect to a wifi
- Update system time with `timedatectl`
- Chage mirror of `pacman` by editing `/etc/pacman.d/mirrorlist`
- Disk partition and make filesystem on them
    - Tools: `lsblk` `mkfs.fat` `mkfs.ext4` `mkswap`
    - Mount each partition on the exact place
- Install a Linux system to `/mnt`
    - Including packages: `base base-devel linux linux-firmware linux-headers networkmanager sudo neovim bash-completion`
- Generate `/mnt/etc/fstab`
- Change `root` to `/mnt`
- Set `/etc/hosts` and `/etc/hostname`
- Link `/etc/localtime`
- Sync time to hardware clock
- Set `/etc/locale.gen` and `/etc/locale.conf`
- Set password
- Install `intel-ucode`
- Install `grub efibootmgr`
    - Install grub to `/boot` partition
    - Edit `/etc/default/grub`
    - Create configuration at `/boot/grub/grub.cfg`
- Exit `/mnt` and `umount -R` every partition
- reboot
- Enable `NetworkManager`

## Customize Installation

- Add your user, make it in `wheel` group.
- `visudo` to enable all commands.

- Add `[multilib]` and `[archlinuxcn]` to pacman.
- Install `archlinuxcn-keyring`
- Sign `farseerfc@archlinux.org` to keyring if required.

- Install Desktop Environment, e.g. Hyprland, waybar
    - font
    - Terminal emulator
    - rofi? wofi? tofi?
    - `pipewire(enable)` `pipewire-alsa` `pipewire-pulse(enable)` `sof-firmware` `alsa-firmware` `alsa-ucm-conf` `wireplumber(enable)`
    - man-db
    - v2raya
    - ffmpeg, then Firefox
    - Fcitx5-im and Fxitx5-rime
    - Enable bluetooth
    - Github dotfiles, openssh and sign key.
    - oh-my-zsh
    - TexLive
    -
