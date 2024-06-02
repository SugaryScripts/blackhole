url:: [GitHub - tj/n: Node version management](https://github.com/tj/n)
[GitHub - mklement0/n-install: Installs n, the Node.js version manager, without needing to install Node.js first: curl -L https://bit.ly/n-install | bash](https://github.com/mklement0/n-install)


# How to use
```sh
n lts
n latest
```
# Install
1. Add this code to .zshrc
```sh
# Whatever your node version is, you'll be using latest npm version regardless (By adding preserve on N code below)
# Because each node are always includes npm npx corepack with their own version
#export N_PRESERVE_NPM=1
#export N_PRESERVE_COREPACK=1
export N_PREFIX="$HOME/.local/.root/.n"; [[ :$PATH: == *":$N_PREFIX/bin:"* ]] || PATH+=":$N_PREFIX/bin"  # Added by n-install (see http://git.io/n-install-repo).
# Pick one package = yarn or npm = to prevent duplicate command or package
export YARN_PREFIX="$HOME/.local/.root/.yarn"; [[ :$PATH: == *":$YARN_PREFIX/bin:"* ]] || PATH+=":$YARN_PREFIX/bin"
export PATH="$HOME/.config/composer/vendor/bin:$PATH"
```
2. download n
```sh
curl -L https://bit.ly/n-install | SHELL=zsh bash
```

3. uninstall
```sh
n-uninstall
```

# Change default location
NPM
```sh
npm --global cache verify
npm config set cache ~/.local/.node/.npm --global
```
YARN
```sh
yarn global dir
yarn config set prefix ~/.local/.node/.yarn
yarn global bin
```
