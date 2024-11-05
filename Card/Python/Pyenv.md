### Linux
#### Install
windows:: [Home · pyenv-win/pyenv-win Wiki · GitHub](https://github.com/pyenv-win/pyenv-win/wiki)
from windows shell, you need to set execution policy first => [[All#Power Shell]]
```sh
pacman -S pyenv
echo 'export PYENV_ROOT="$HOME/.local/.pyenv"' >> ~/.zshrc
echo '[[ -d $PYENV_ROOT/bin ]] && export PATH="$PYENV_ROOT/bin:$PATH"' >> ~/.zshrc
echo 'eval "$(pyenv init -)"' >> ~/.zshrc

python --version
pyenv install --list
pyenv install 3.12.2

nvim ~/.local/.pyenv/version
3.12.2 -> :wq
python --version
```
#### Change version
Set local version for project
```sh
pyenv local <version>
```
Set global version
```sh
pyenv global <version>
```
#### Uninstall
```sh
pyenv uninstall $python_version
```
Remove pyenv manual
```sh
rm -rf ~/.pyenv/versions/"X.Y.Z"
```
### Read More
source:: [GitHub - pyenv/pyenv: Simple Python version management](https://github.com/pyenv/pyenv)

### Windows
#### Install 
[[All]]
```
Invoke-WebRequest -UseBasicParsing -Uri "https://raw.githubusercontent.com/pyenv-win/pyenv-win/master/pyenv-win/install-pyenv-win.ps1" -OutFile "./install-pyenv-win.ps1"; &"./install-pyenv-win.ps1"
```
Check variables environment for pyenv and it's directory location
### Uninstall
Remove .pyenv folder
Clear the desktop environment variables too