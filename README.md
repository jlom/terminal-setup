A short summary of my terminal setup. This is mostly just for my own future reference.

![Screenshot](Screen Shot 2016-06-04 at 23.18.45 .png)

## iTerm settings

- Appearance 
  - Tabs
    - Theme: Dark 

- Profiles
  - Colors
    - Color Presets… -> Import -> [Japanesque](https://github.com/mbadolato/iTerm2-Color-Schemes/blob/master/schemes/Japanesque.itermcolors)

- Text
  - Cursor: Underline
  - Font: 10pt [Droid Sans Mono Awesome](https://github.com/gabrielelana/awesome-terminal-fonts/tree/patching-strategy/patched)
  - Use thin strokes for anti-aliased text: Always
  - Uncheck "Use a different font for non-ASCII text"

- Terminal
  - Report Terminal Type: `xterm-256color`

- Keys
  - `⌘ + Backspace`: Send Hex Codes: `0x15` _(Erase to start of line)_
  - `⌥ + Backspace`: Send Hex Codes `0x1b 0x88` _(Erase one word back)_
  - `⌘ + ←`: Send Hex Codes: `0x01` _(Cursor to start of line)_
  - `⌘ + →`: Send Hex Codes: `0x05` _(Cursor to end of line)_
  - `⌥ + ←`: Send Hex Codes: `0x1b 0x62` _(Cursor one word back)_
  - `⌥ + →`: Send Hex Codes: `0x1b 0x66` _(Cursor one word forward)_

- Advanced
  Use "smart truncation" for tab titles
  Terminal windows resize smoothly

## Zsh
Install [Oh My Zsh](http://ohmyz.sh/):
```sh
$ sh -c "$(curl -fsSL https://raw.github.com/robbyrussell/oh-my-zsh/master/tools/install.sh)"
```

Install [zsh-autosuggestions](https://github.com/zsh-users/zsh-autosuggestions):
```sh
$ git clone git://github.com/zsh-users/zsh-autosuggestions $ZSH_CUSTOM/plugins/zsh-autosuggestions
```

Install [Powerlevel 9K](https://github.com/bhilburn/powerlevel9k):
```sh
$ git clone https://github.com/bhilburn/powerlevel9k.git ~/.oh-my-zsh/custom/themes/powerlevel9k
```

Install [zsh-syntax-highlighting](https://github.com/zsh-users/zsh-syntax-highlighting/):
```sh
$ git clone https://github.com/zsh-users/zsh-syntax-highlighting.git ${ZSH_CUSTOM:-~/.oh-my-zsh/custom}/plugins/zsh-syntax-highlighting
```

Other [really](https://github.com/posva/catimg), [really](https://en.wikipedia.org/wiki/Cowsay) [useful](https://github.com/passy/givegif) tools: 🐮
```sh
$ brew tap passy/givegif && brew install catimg cowsay givegif
```

~/.zshrc:
```
export ZSH=~/.oh-my-zsh
ZSH_THEME="powerlevel9k/powerlevel9k"
POWERLEVEL9K_MODE='awesome-patched'
POWERLEVEL9K_STATUS_VERBOSE=false
POWERLEVEL9K_LEFT_PROMPT_ELEMENTS=(context dir root_indicator)
POWERLEVEL9K_RIGHT_PROMPT_ELEMENTS=(status vcs time)
POWERLEVEL9K_STATUS_VERBOSE=false
POWERLEVEL9K_HIDE_BRANCH_ICON=true
DEFAULT_USER=$USER
POWERLEVEL9K_SHORTEN_DIR_LENGTH=2
POWERLEVEL9K_SHORTEN_STRATEGY="truncate_from_right"
HIST_STAMPS="dd.mm.yyyy"
plugins=(git zsh-autosuggestions zsh-syntax-highlighting)
export PATH="/usr/local/bin:/usr/bin:/bin:/usr/sbin:/sbin:/usr/local/MacGPG2/bin"
source $ZSH/oh-my-zsh.sh
```
