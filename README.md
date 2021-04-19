# Configuration files to miscellaneous tools I use.
Hiddned files do not have the `.` prefix for easier navigation.

## Vim
Vim plugins are added as git submodules. E.g. NERDTree:

`git submodule add git@github.com:preservim/nerdtree.git vim/vim/pack/NERDTree/start/NERDTree`

After cloning don't forget `git submodule init` followed by `git submodule update`.

 * Linux
    * `ln -s ~/configuration_files/vim/vim ~/.vim`
    * `ln -s ~/configuration_files/vim/vimrc ~/.vimrc`
 * Cygwin/MSYS2
    * `cmd //c 'mklink /D %HOME%\.vim %HOME%\configuration_files\vim\vim'`
    * `cmd //c 'mklink %HOME%\.vimrc %HOME%\configuration_files\vim\vimrc'`

### Patches
Folder `vim/patch` contains optional patches. Install it to respective repository. E.g. in CtrlP plugin:

`git apply ~/configuration_files/vim/patch/ctrlp/statusline.patch`

## Tmux
Use `tmux_start` script to start or attach to the session. Use `tmux_end` to destroy the session.

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
