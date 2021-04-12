# Configuration files to miscellaneous tools I use.
Hiddned files do not have the `.` prefix for easier navigation.

## Vim

## Tmux
Use `tmux_start` script to start or attach to the session.
 * Linux `ln -s ~/configuration_files/tmux/tmux.conf ~/.tmux.conf`
 * Cygwin/MSYS2 `cmd //c 'mklink %HOME%/.tmux.conf %HOME%/configuration_files/tmux/tmux.conf'`

## Bash
If `~/.bash_profile` is present `~/.profile` is not executed. Place this code respectively.
```bash
if [ -f "$HOME/.profile.local" ]; then
    . $HOME/.profile.local
fi
```
 * Linux `ln -s ~/configuration_files/bash/profile.local ~/.profile.local`
 * Cygwin/MSYS2 `cmd //c 'mklink %HOME%/.profile.local %HOME%/configuration_files/bash/profile.local'`
