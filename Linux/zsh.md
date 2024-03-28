
# oh my zsh

`zsh` can change its config files to another directory, a big pro for me.
To do so, just place these in `.zshenv` and `source` it.

```shell
export ZDOTDIR="$HOME/.config/zsh"

export XDG_CACHE_HOME="$HOME/.cache"
export XDG_CONFIG_HOME="$HOME/.config"
export XDG_DATA_HOME="$HOME/.local/share"

export EDITOR=nvim
```
