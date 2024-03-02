## Eas
```sh
eas login
eas init --id ...-...-...
eas build => all done and make apk
eas build:configure
eas update:configure
eas update | update --auto
eas branch:list | delete
eas branch:rename --from [name] --to [name]
eas channel:list
eas channel:edit production --branch version-2.0
```
## yarn
```sh
yarn global dir
yarn config set prefix ~/.local/.root/.yarn
yarn global bin

yarn global list
yarn global add [package]
yarn global upgrade
yarn global uprade-interactive
yarn global remove [package]
yarn remove [package]
yarn add [package]
yarn add [package] --dev
```
## npm
```sh
npm config set cache ~/.local/.root/.npm --global
npm --global cache verify
```
##### global
```sh
npm outdated -g --depth=0
npm ls -g --depth=0
npm i -g [package]
npm update -g <package_name>
```
##### update all
```sh
npm update -g
```
##### local
```sh
npm outdated
npm update
npm uninstall [package]
npm i [package] --save
npm i [package] --save-dev
```

## N
```sh
curl -L https://bit.ly/n-install | SHELL=zsh bash
n -V
n-update
n-uninstall
```
##### install lts node version
`n lts`
##### Uninstall other node version 
`n prune`

