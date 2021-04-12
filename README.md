# Configuration files to miscellaneous tools I use.
Hiddned files do not have the `.` prefix for easier navigation.

## Vim

## Tmux
Use `tmux_start` script to start or attach to the session.

 * Linux `ln -s ~/configuration_files/tmux/tmux.conf ~/.tmux.conf`
 * Cygwin/MSYS2 `cmd //c 'mklink %HOME%/.tmux.conf %HOME%/configuration_files/tmux/tmux.conf'`

## Bash
Non-login shells execute `~/.bashrc` where login shells
execute `~/.profile` or `~/.bash_profile` which (almost) always call `~/.bashrc`.

 * Linux `ln -s ~/configuration_files/bash/bashrc.local ~/.bashrc`
 * Cygwin/MSYS2 `cmd //c 'mklink %HOME%/.bashrc.local %HOME%/configuration_files/bash/bashrc.local'`

or in your current `~/.bashrc`
```bash
if [ -f "$HOME/configuration_files/bash/bashrc.local" ]; then
    . $HOME/configuration_files/bash/bashrc.local
fi
```
