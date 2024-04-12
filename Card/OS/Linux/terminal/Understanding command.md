# Case
## git clone power level 10 k - zsh
```sh
git clone --depth=1 https://github.com/romkatv/powerlevel10k.git ${ZSH_CUSTOM:-$HOME/.oh-my-zsh/custom}/themes/powerlevel10k
```

- **[[#--depth]]=1:** clone latest version and (**not its entire history**)
- **`${ZSH_CUSTOM:-$HOME/.oh-my-zsh/custom}/themes/powerlevel10k:`** This is the destination path where the downloaded theme files will be placed. Here's how it works:
	- `$ZSH_CUSTOM`: This is an environment variable that might be set by Oh My Zsh to point to the custom themes directory.
	- `:-$HOME/.oh-my-zsh/custom` : This is a fallback path in case `$ZSH_CUSTOM` is not set. It specifies the default custom themes directory within Oh My Zsh.
	- `/themes/powerlevel10k`: This creates a subdirectory named "powerlevel10k" within the custom themes directory to store the downloaded theme files.

# Git
## clone
### --depth
This option tells `git clone` to only download the latest version of the repository (master branch) and not its entire history. This saves on download time and disk space.

# Basic
## Enviroment Variable
