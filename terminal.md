# Setting up the Perfect MacOS Terminal

## 1. The Terminal Application

The first step to a better MacOS terminal experience is getting a better terminal app. In my opinion, the terminal included with MacOS just doesn't have enough features. My two terminals of choice include iTerm2 and Hyper.

1. Download [iTerm 2](https://www.iterm2.com) or [Hyper](https://hyper.is)
1. Unzip and drag to Applications Folder

## 2. Install Homebrew

1. Run `/usr/bin/ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"`

## 3. Preparing Zsh

1. Run `brew install zsh zsh-completions` to update Zsh
1. Run `zsh --version` and verify that the version returned is `5.7.1` or newer
1. Run `chsh -s $(which zsh)` to set Zsh as your default shell
1. Restart your computer
1. Run `echo $SHELL` to verify that it worked

## 4. Installing Oh my Zsh

1. Run `sh -c "$(curl -fsSL https://raw.githubusercontent.com/robbyrussell/oh-my-zsh/master/tools/install.sh)"` to install Oh my Zsh

## 5. Installing Spaceship Prompt

1. Run `git clone https://github.com/denysdovhan/spaceship-prompt.git "$ZSH_CUSTOM/themes/spaceship-prompt"`
1. Run `ln -s "$ZSH_CUSTOM/themes/spaceship-prompt/spaceship.zsh-theme" "$ZSH_CUSTOM/themes/spaceship.zsh-theme"`
1. Run `nano ~/.zshrc` and change `ZSH_THEME="spaceship"`
1. Restart your terminal

## 6. Make the theme better

1. Install the font Monoid from `https://www.nerdfonts.com/font-downloads`
1. Run `sudo gem install colorls`
1. Run `nano ~/.zshrc`
1. Add the following text below the theme section

```
SPACESHIP_PROMPT_ADD_NEWLINE="true"
SPACESHIP_CHAR_SYMBOL=" \uf0e7"
SPACESHIP_CHAR_PREFIX="\uf296"
SPACESHIP_CHAR_SUFFIX=(" ")
SPACESHIP_CHAR_COLOR_SUCCESS="yellow"
SPACESHIP_PROMPT_DEFAULT_PREFIX="$USER"
SPACESHIP_PROMPT_FIRST_PREFIX_SHOW="true"
SPACESHIP_USER_SHOW="true"
```

5. Add the following text at the very bottom
```
alias ls='colorls'
alias lc='colorls --tree'
```

## 7. Install the Color Theme

1. Download `https://raw.githubusercontent.com/nathanbuchar/atom-one-dark-terminal/master/scheme/iterm/One%20Dark.itermcolors`
2. Import to iTerm

## References

- https://medium.com/@caulfieldOwen/youre-missing-out-on-a-better-mac-terminal-experience-d73647abf6d7
