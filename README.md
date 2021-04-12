# Configuration files to miscellaneous tools I use.
Hiddned files do not have the `.` prefix for easier navigation.

## Vim

## Tmux
Use `tmux_start` script to start or attach to the session.

### Install
 * Linux `ln -s ~/configuration_files/tmux/tmux.conf ~/.tmux.conf`
 * Cygwin/MSYS2 `cmd //c 'mklink %HOME%/.tmux.conf %HOME%/configuration_files/tmux/tmux.conf'`

## Bash
Non-login shells execute `~/.bashrc` where login shells
execute `~/.profile` or `~/.bash_profile` which (almost) always call `~/.bashrc`.

###Install
 * Linux `ln -s ~/configuration_files/bash/bash.local ~/.bashrc`
 * Cygwin/MSYS2 `cmd //c 'mklink %HOME%/.bashrc.local %HOME%/configuration_files/bash/bashrc.local'`

or in your current `~/.bashrc`
```bash
if [ -f "~/configuration_files/bash/bash.local" ]; then
    . ~/configuration_files/bash/bash.local
fi
```
