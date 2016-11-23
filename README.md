# Dotfiles!

These are my personal dotfiles.

These dotfiles are best used with zsh,
[oh-my-zsh](https://github.com/robbyrussell/oh-my-zsh), and the
[solarized](http://ethanschoonover.com/solarized) colorscheme. The configuration
has [powerline](https://github.com/powerline/powerline) active for vim and tmux,
and uses a custom zsh theme similar to agnoster. Thus you'll need to patch to a
font that supports powerline.

## Installation
Installation is as simple as cloning the repo and running the setup script. The
script will fetch oh-my-zsh and symlink the dotfiles to your home directory. You
will need to set up solarized and compatible fonts beforehand, however. There
are files in the `new_machine` directory that can be used to set those up.

```bash
git clone https://github.com/jakrach/dotfiles.git --recursive ~/.dotfiles
cd ~/.dotfiles
./setup.sh
```

If you forgot to clone the submodules, you can run `git submodule update --init`
to get them after cloning the main repo.

## Customizing
You can customize vim, git, and zsh for each specific machine. Just put any
additional configurations in `~/.zshrc.local`, `~/.gitconfig.local`, and
`~/.vimrc.local`. Sample local configs are included in this repo.

## Teardown
To clean up the dotfiles, run the teardown script. It will remove all symlinks,
but zsh and oh-my-zsh will be untouched.

```bash
cd ~/.dotfiles
./teardown.sh
rm -rf ~/.oh-my-zsh # optionally remove oh-my-zsh
chsh -s `which bash` # optionally change shell back to bash
```

## Other dotfiles
Here are some repos that I cherry-pick useful stuff from. :)
* [Unofficial Dotfile Guide](http://dotfiles.github.io/)
* [Nick's Dotfiles](https://github.com/nicksp/dotfiles)
* [Ryan's Dotfiles](https://github.com/ryanb/dotfiles)
* [YADR](https://github.com/skwp/dotfiles)

