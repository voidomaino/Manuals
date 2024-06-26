# 存储设备

管理存储设备的第一步是把设备挂载到 [[file_system| 文件系统树]] 中。

只要存储设备通过某种接口连接到了电脑上，它就会显示在 `/dev/` 目录下。若要读写设备，就使用 `mount` 命令将设备挂载到文件系统的某个目录下，设备的文件系统于是接入主文件系统，并能够访问和读写。

有一个叫做 `/etc/fstab` 的文件可以列出系统启动时要挂载的设备。

`mount` 命令被用来挂载文件系统。执行这个不带参数的命令，将会显示一系列当前挂载的
文件系统，包括设备名称、挂载点和文件系统类型。

`umount` 命令用于卸载一个设备。

## 格式化存储设备

`fdisk` 操作设备分区。

`mkfs` 创建一个新的文件系统。

## 克隆设备

`dd` 将数据从一个设备复制到另一个。或者将设备内的数据创建为一个 `.iso` 文件。