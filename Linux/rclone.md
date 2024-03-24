
# rclone

## Grammar

```shell
# local to cloud
rclone [function] <local path> <setup:path> [parameters]
# cloud to local 
rclone [function] <setup:path> <local path> [parameters]
# cloud to cloud
rclone [function] <setup:path> <setup:path> [parameters]
```

### Functions

copy: copy

move: move, if you want to delete empty source directory after moving, append
parameter `--delete-empty-src-dirs`

mount: mount

sync: synchronize, only change target directory

check: check consistency of source and target data

size: query size of cloud files

delete: delete file

purge: delete directory and all files inside

mkdir: create directory

rmdir: delete directory

rmdirs: delete empty directories

ls: list all files and directories under given path

lsl: same as `ls`, appending upload time

lsd: list directories under given path

lsf: list files and directories under given path

### Parameters

`-n` as `--dry-run`: test run, see what will happen

`-P` as `--progress`: display transfer speed, update every 500 ms

`--config`: set configuration path

`--ignore-errors`: literally

`--size-only`: only check file size instead of hash

rclone has 4 levels of log files `ERROR`, `NOTICE`, `INFO`, and `DEBUG`

only `ERROR` and `NOTICE` will be created by default

`-q`: only create `ERROR`

`-v`: create `ERROR`, `NOTICE` and `INFO`

`-vv`: create all

`--log-level <LEVEL>`: appoint log level
