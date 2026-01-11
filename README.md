# Set up Mac OS

## iTerm2

* Install iTerm2
* Download [Nord](https://www.nordtheme.com/ports) color theme 
* Download [CaskaydiaCove Nerd Font](https://github.com/ryanoasis/nerd-fonts/releases/download/v3.3.0/CascadiaCode.zip)
* Import Them into iTerm2, and change profiles for using them

## Development Environment

1. Install Homebrew
```
$ /bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"
```

2. Install tmux & plugins
```
$ brew install tmux
$ git clone https://github.com/tmux-plugins/tpm ~/.tmux/plugins/tpm
$ cp ./dotfiles/.tmux.conf ~/
```
Open tmux and execute prefix + I

3. Install NeoVim
```
$ brew install neovim
$ mkdir -p ~/.config/nvim/
$ cp -r ../dotfiles/nvim ~/.config/nvim/
```
Open nvim then plugions will be automaticaly installed

4. Install uv and python
```
$ curl -LsSf https://astral.sh/uv/install.sh | sh

# default option is an experimental feature to use python installed by uv as a global python
$ uv python install 3.14 --default --preview-features 
```

5. Install Powerline

I install powerline by using "uv tool" without "pip install --user". The uv also has pip interface but it doesn't have user option. The pip of uv just installs packages into virtual environments. 
```
$ uv tool install powerline-shell
```

6. Install nvm and Node.js

Install [nvm](https://github.com/nvm-sh/nvm) and the latest Node.js.
```
$ curl -o- https://raw.githubusercontent.com/nvm-sh/nvm/v0.40.3/install.sh | bash
$ nvm install node # "node" is an alias for the latest version
```

7. Move .zshrc
```
$ cp ./dotfiles/.zshrc ~/
```

8. Install Go

Download latest stable version golang from [donwload page](https://go.dev/doc/install) and install it.

9. Install Rust
```
$ curl --proto '=https' --tlsv1.2 https://sh.rustup.rs -sSf | sh
```
