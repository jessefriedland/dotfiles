Dotfiles
========

## Overview

1. [Brew](http://brew.sh/) mac package manager that will install the packages listed in the [Brewfile](https://github.com/jessefriedland/dotfiles/blob/master/packages/Brewfile) and any packages installed in files in your $HOME directory that match .Brewfile.*local file pattern

2. Your [bash_profile](https://github.com/jessefriedland/dotfiles/blob/master/shell/bash_profile) which will source several other bash settings from the [shell folder](https://github.com/jessefriedland/dotfiles/blob/master/shell)

3. Gems listed in the [Gemfile](https://github.com/jessefriedland/dotfiles/blob/master/packages/Gemfile) and any gems installed in files in your $HOME directory that match .Gemfile.*local file pattern

4. Mac applications (Casks) listed in the [Caskfile](https://github.com/jessefriedland/dotfiles/blob/master/applications/Caskfile) and any casks installed in files in your $HOME directory that match .Caskfile.*local file pattern

5. [Vim](https://github.com/jessefriedland/dotfiles/tree/master/vim)

## Setup

##### How to setup on personal laptop

1) Execute the following command replacing $USERNAME with your github username to install and initalize all dotfiles components

```
bash -c "$(curl -u $USERNAME -p -fsSL https://github.com/raw/jessefriedland/dotfiles/master/bin/dotfiles)"
```

2) Profit.

3.optional) Create your own dotfiles.*local repository! You can fork [Jesse's local dotfiles](https://github.com/jessefriedland/dotfiles.local) to get started.
* After forking, make sure to change the GIT_USER and GIT_ORG in [dotfiles](https://github.com/jessefriedland/dotfiles.local/blob/master/bin/dotfiles.local) script
* Also, make sure to remove or alter anything specific to jesse like [this](https://github.com/jessefriedland/dotfiles.local/blob/master/gitconfig.local)

3.optional) Create local configurations for your bash profile or gitconfig
* ~/.gitconfig.local
* ~/.bash_profile.local
```

## Updating

##### No Installs Update

Execute this to get the latest dotfiles with no Software or Package updates. See the help `~/.dotfiles/bin/dotfiles --help` for more options
```
~/.dotfiles/bin/dotfiles --no-installs
```

### References

This is forked from https://github.com/necolas/dotfiles
