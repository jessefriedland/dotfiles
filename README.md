Dotfiles
========

## Overview

The Dotfiles repository sets you up for success ... okay, kidding ... the Dotfiles repository sets up the following things:

1. [Brew](http://brew.sh/) mac package manager that will install the packages listed in the [Brewfile](https://github.bamtech.co/multimedia-development/dotfiles/blob/master/packages/Brewfile) and any packages installed in files in your $HOME directory that match .Brewfile.*local file pattern

2. Your [bash_profile](https://github.bamtech.co/multimedia-development/dotfiles/blob/master/shell/bash_profile) which will source several other bash settings from the [shell folder](https://github.bamtech.co/multimedia-development/dotfiles/blob/master/shell)

3. Gems listed in the [Gemfile](https://github.bamtech.co/multimedia-development/dotfiles/blob/master/packages/Gemfile) and any gems installed in files in your $HOME directory that match .Gemfile.*local file pattern

4. Mac applications (Casks) listed in the [Caskfile](https://github.bamtech.co/multimedia-development/dotfiles/blob/master/applications/Caskfile) and any casks installed in files in your $HOME directory that match .Caskfile.*local file pattern

5. [Vim](https://github.bamtech.co/multimedia-development/dotfiles/tree/master/vim)

## Setup

##### How to setup on personal laptop

1) If you are would like the [mm-dev setup](https://github.bamtech.co/multimedia-development/dotfiles.mmdev.local), execute the following command replacing $USERNAME with your ldap username
      * This sets up symlinks between the mmdev local dotfiles and your $HOME directory
    
    
```
bash -c "$(curl -u $USERNAME -p -fsSL https://github.bamtech.co/raw/multimedia-development/dotfiles.mmdev.local/master/bin/dotfiles.local)"
```

2) Execute the following command replacing $USERNAME with your LDAP username to install and initalize all dotfiles components

```
bash -c "$(curl -u $USERNAME -p -fsSL https://github.bamtech.co/raw/multimedia-development/dotfiles/master/bin/dotfiles)"
```

3) Profit.

4.optional) Create your own dotfiles.*local repository! You can fork [Jesse's local dotfiles](https://github.bamtech.co/jfriedla/dotfiles.local) to get started.
* After forking, make sure to change the GIT_USER and GIT_ORG in [dotfiles](https://github.bamtech.co/jfriedla/dotfiles.local/blob/master/bin/dotfiles.local) script
* Also, make sure to remove or alter anything specific to jesse like [this](https://github.bamtech.co/jfriedla/dotfiles.local/blob/master/gitconfig.local)

5.optional) Create local configurations for your bash profile or gitconfig
* ~/.gitconfig.local
* ~/.bash_profile.local

#### How to setup on mlbam remote server

1) Execute the following command replacing $USERNAME with your LDAP username to install and initalize all non-brew dotfiles components

MM3:
```bash
curl -u `whoami` -p -fsSL -x "https://proxy-vip.mm3.mlbam.com:80" https://github.bamtech.co/raw/multimedia-development/dotfiles/master/bin/dotfiles -o /tmp/dotfiles && /tmp/dotfiles
```
Media 3:
```bash
curl -u `whoami` -p -fsSL -x "https://proxy-vip.med3.util.mlbam.net:80" https://github.bamtech.co/raw/multimedia-development/dotfiles/master/bin/dotfiles -o /tmp/dotfiles && /tmp/dotfiles --no-brew
```

## Updating

##### No Installs Update

Execute this to get the latest dotfiles with no Software or Package updates. See the help `~/.dotfiles/bin/dotfiles --help` for more options
```
~/.dotfiles/bin/dotfiles --no-installs
```

## Contributing

In order to contribute to this script / repository, you should send pull requests describing why the additions or changes are important to the core framework. You should ask yourself, are these changes good for any developer or would they be better suited in the [mmdev specific dotfiles](https://github.bamtech.co/multimedia-development/dotfiles.mmdev.local) or perhaps in your own dotfiles like [Jesse's personal dotfiles](https://github.bamtech.co/jfriedla/dotfiles.local)

### References

This is forked from https://github.com/necolas/dotfiles
