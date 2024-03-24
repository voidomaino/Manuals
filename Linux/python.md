
# 部署 python

使用 `pip` 来安装 python 包可能和发行版的包管理器冲突。

## 普通用户给自己安装

```bash
pip install --user packagename
```

Installing in your home will not conflict with the package manager.

By default pip install --user will install in your "user site" directory.
Usually that is something like: /home/lesmana/.local/lib/python3.6/site-packages.

The following command will print, among others, your "user site" location:

```bash
python -m site
```

To customize the install location:

```bash
PYTHONUSERBASE=$HOME/some/dir pip install --user packagename
```

this will install everything under `$HOME/some/dir`

to run:

```bash
PYTHONUSERBASE=$HOME/some/dir $HOME/some/dir/bin/progname
```

## 普通用户给所有人安装

if you do want the python package for all users then the best place to install it is `/opt`. for example like this:

```bash
PYTHONUSERBASE=/opt/packagedir pip install packagename
# note the missing --user
```

and to run, as above:

```bash
PYTHONUSERBASE=/opt/packagedir /opt/packagedir/bin/progname
```

Background explanation: `/opt` is commonly acknowledged by gnu/linux distributions as the directory where the local user or system administrator can install his own stuff.
In other words: the package manager of distributions usually do not touch `/opt`. this is more or less standardized in the Filesystem Hierarchy Standard.

For comfort of the users you will still want to write a wrapper script and place it in `/bin` or `/usr/bin`.
This still bears risk of colliding with the distribution package manager but at least it is just one wrapper script file.
So the damage that might be done is minimal.
You can name the wrapper script something like local-foo or custom-foo to further minimize the risk of collision with the distribution package manager.

Alternatively you can modify PATH to include /opt/bin and place your wrapper script there. But this again requires you to modify a (or some) system files where PATH is defined which again may be overwritten by the distribution package manager.

In short: if you want to install for all users then do so in /opt. Where you place the wrapper script for comfort is a judgement call.

More Information about /opt and Filesystem Hierarchy Standard:
