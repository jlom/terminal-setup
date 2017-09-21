A short summary of my terminal setup. This is mostly just for my own future reference.

![Screenshot](https://github.com/jlom/terminal-setup/blob/master/Screen%20Shot%202016-06-04%20at%2023.18.45%20.png)

## iTerm settings
- Set the tab appearance to dark: *Appearance → Tabs → Theme: Dark*
- Install [Droid Sans Mono Awesome](https://github.com/gabrielelana/awesome-terminal-fonts/tree/patching-strategy/patched)
- Drop `iTermProfile.json` into `~/Library/Application Support/iTerm2/DynamicProfiles`

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

Install [marker](https://github.com/pindexis/marker):
```sh
$ git clone https://github.com/pindexis/marker ~/.marker
$ ~/.marker/install.py
```

Install [The Fuck](https://github.com/nvbn/thefuck), and other [really](https://github.com/posva/catimg), [really](https://en.wikipedia.org/wiki/Cowsay) [useful](https://github.com/passy/givegif) tools: 🐮
```sh
$ brew tap passy/givegif && brew install catimg cowsay givegif thefuck
```

Finally copy the [.zshrc](.zshrc)-file to the home dir.
