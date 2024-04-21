## Terminal

Preparation
```sh
sudo pacman -Syu && sudo pacman -S zsh
```


#### .Xresources
```json
URxvt.font: 					  xft:MesloLGS NF:size=11

URxvt*scrollBar:                  true

URxvt*inheritPixmap:            true
URxvt*transparent:              true
URxvt*shading:                  25
```

#### Zsh [[Shell ZSH]]
```sh
chsh -s /bin/zsh
```

#### Install Oh my zsh

```sh
sh -c "$(curl -fsSL https://raw.github.com/ohmyzsh/ohmyzsh/master/tools/install.sh)"
```
or
```sh
sh -c "$(wget https://raw.github.com/ohmyzsh/ohmyzsh/master/tools/install.sh -O -)"
```


#### Custom Theme - power level 10k
source = [GitHub - romkatv/powerlevel10k: A Zsh theme](https://github.com/romkatv/powerlevel10k)

1. [[#.Xresources|Install the recommended font]]. _Optional but highly recommended._ (MesloLGS NF fonts)
2. [[#Install Powerlevel10k]] itself.
3. Restart Zsh with `exec zsh`.
4. Type `p10k configure` if the configuration wizard doesn't start automatically.


##### Sub tasks
###### Install Powerlevel10k

1. Download power level 10k - oh my zsh
```sh
git clone --depth=1 https://github.com/romkatv/powerlevel10k.git ${ZSH_CUSTOM:-$HOME/.oh-my-zsh/custom}/themes/powerlevel10k
```
Read more about what this command do [[Understanding command#git clone power level 10 k - zsh|HERE]]

2. Set `ZSH_THEME="powerlevel10k/powerlevel10k"` in `~/.zshrc`.




#### Customize ZSH
[[#ZSH Plugins|SOURCES]]

##### Crucial plugins
```sh
git clone https://github.com/zsh-users/zsh-syntax-highlighting.git ${ZSH_CUSTOM:-~/.oh-my-zsh/custom}/plugins/zsh-syntax-highlighting
```

```sh
git clone https://github.com/zsh-users/zsh-autosuggestions ${ZSH_CUSTOM:-~/.oh-my-zsh/custom}/plugins/zsh-autosuggestions
```

Modify the `~/.zshrc` config file editting plugins section like this:

```json
plugins=(
    git
    zsh-autosuggestions
    zsh-syntax-highlighting
)
```

```sh
source ~/.zshrc
```

##### FZF find with ease
url:: [GitHub - junegunn/fzf: :cherry\_blossom: A command-line fuzzy finder](https://github.com/junegunn/fzf)
readme:: [[fzf readme]]
usage:: [[FZF]]
Specific in manjaro
```sh
pacman -Ss fzf
pacman -S fzf
```
Add these to .zshrc
```sh
source /usr/share/fzf/key-bindings.zsh
source /usr/share/fzf/completion.zsh
```

##### Bat
url:: [GitHub - sharkdp/bat: A cat(1) clone with wings.](https://github.com/sharkdp/bat)
readme:: [[bat readme]]
usage:: [[BAT]]

##### The fuck
url:: [GitHub - nvbn/thefuck: Magnificent app which corrects your previous console command.](https://github.com/nvbn/thefuck?tab=readme-ov-file)


## Worth reading or explored
### ZSH Plugins

[Set Up and Beautify ZSH in Manjaro Linux | by Rumaisa Niazi | Medium](https://rumaisaniazi008.medium.com/set-up-and-beautify-zsh-in-manjaro-linux-10c7ae87db56)
[Top Popular ZSH Plugins on GitHub (2023)](https://safjan.com/top-popular-zsh-plugins-on-github-2023/)
[10 Zsh Tips & Tricks: Configuration, Customization & Usage — SitePoint](https://www.sitepoint.com/zsh-tips-tricks/)
