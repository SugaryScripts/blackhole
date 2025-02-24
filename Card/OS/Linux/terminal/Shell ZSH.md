#### Basic
[Supercharge your command line - DEV Community](https://dev.to/budavariam/supercharge-your-command-line-2c9b)


```sh
echo $SHELL
chsh -l
chsh -s /bin/zsh
exec zsh
```
or 
```sh
chsh -s $(which zsh)
```

Change fonts to 
```json
URxvt.font: 					  xft:MesloLGS NF:size=11
```

#### Rerun first setup wizard
[Run the Zsh first use wizard - Unix & Linux Stack Exchange](https://unix.stackexchange.com/questions/108136/run-the-zsh-first-use-wizard)
The wizard is provided by the function [`zsh-newuser-install`](http://zsh.sourceforge.net/Doc/Release/User-Contributions.html#User-Configuration-Functions).

To run it again, make a backup of your `.zshrc` (because there's a small risk that `zsh-newuser-install` will mess up your manual configuration), then run

```bash
autoload -U zsh-newuser-install
zsh-newuser-install -f
```

#### Plugins
[Plugins · ohmyzsh/ohmyzsh Wiki · GitHub](https://github.com/ohmyzsh/ohmyzsh/wiki/Plugins)
