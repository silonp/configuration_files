# Configuration files to miscellaneous tools I use.
Hiddned files do not have the `.` prefix for easier navigation.

## Vim
Vim plugins are added as git submodules. E.g:

`git submodule add git@github.com:preservim/nerdtree.git vim/vim/pack/NERDTree/start/NERDTree`

 * Linux `ln -s ~/configuration_files/vim/vim ~/.vim` and `ln -s ~/configuration_files/vim/vimrc ~/.vimrc`
 * Cygwin/MSYS2 `TODO`
     
## Tmux
Use `tmux_start` script to start or attach to the session. Use `tmux_end` to destory the session.

 * Linux `ln -s ~/configuration_files/tmux/tmux.conf ~/.tmux.conf`
 * Cygwin/MSYS2 `cmd //c 'mklink %HOME%\.tmux.conf %HOME%\configuration_files\tmux\tmux.conf'`

## Bash
Non-login shells execute `~/.bashrc` where login shells
execute `~/.profile` or `~/.bash_profile` which (almost) always call `~/.bashrc`.

 * Linux `ln -s ~/configuration_files/bash/bashrc.local ~/.bashrc`
 * Cygwin/MSYS2 `cmd //c 'mklink %HOME%\.bashrc.local %HOME%\configuration_files\bash\bashrc.local'`

or in your current `~/.bashrc`
```bash
if [ -f "$HOME/configuration_files/bash/bashrc.local" ]; then
    . $HOME/configuration_files/bash/bashrc.local
fi
```
## Git
Global git configuration.

 * Linux `ln -s ~/configuration_files/git/gitconfig ~/.gitconfig`
 * Cygwin/MSYS2 `cmd //c 'mklink %HOME%\.gitconfig %HOME%\configuration_files\git\gitconfig'`
