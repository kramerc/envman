# envman

An environment manager crafted to my needs.

## Installation

1. Clone envman to your home directory

   ```
   git clone https://github.com/kramerc/envman.git ~/.envman
   ```

2. Symlink envman to a directory in `$PATH`, (e.g., `~/.local/bin`)

   ```
   mkdir -p ~/.local/bin
   ln -s ~/.envman/bin/envman ~/.local/bin
   ```

3. Configure envman (see the [Configuration](#configuration) section below for options)
   ```
   cp ~/.envman/templates/.envmanrc ~/.envmanrc
   vim ~/.envmanrc
   ```

4. Run envman for the first time

   ```
   envman
   ```

## Configuration

envman can be configured in the `.envmanrc` file in your home directory. Boolean options should be set to `1` for true and `0` for false.

### dotfiles
* `DOTFILES_DIR` - Where to store managed dotfiles  
  **Default:** `~/.dotfiles`


* `DOTFILES_REPO` - Remote repository URL for dotfiles


* `DOTFILES` - Array of dotfiles to manage  
  These should be a list of files and paths without the leading `.`


* `VIM_DIR` - Path of `.vim`   
  **Default:** `~/.vim`


* `VIM_BUNDLE_DIR` - Path of `.vim/bundle`  
  **Default:** `~/.vim/bundle`


* `VUNDLE` - (Boolean) Whether to install Vundle if it's not present


* `VUNDLE_INSTALL_PLUGINS` - (Boolean) Install Vundle plugins on first install?

### zsh

* `OH_MY_ZSH` - (Boolean) Whether to install oh-my-zsh if it's not present


* `OH_MY_ZSH_DIR` - Path to oh-my-zsh  
  **Default:** `~/.oh-my-zsh`


* `OH_MY_ZSH_CUSTOM_PLUGINS` - Array of custom oh-my-zsh plugins, all of which should be Git repos  
  The format for each entry is `name|url`


* `OH_MY_ZSH_CUSTOM_THEMES` - Array of custom oh-my-zsh themes, all of which should be direct raw links  
  The format for each entry is `name|url`
