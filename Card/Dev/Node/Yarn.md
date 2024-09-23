###### Install (classic)
```sh
npm i -g yarn
```
###### global
```sh
yarn global add
yarn global list
```

###### yarn 4 (new install)
```sh
# npm i -g corepack -> if corepack doesnt found
corepack enable
yarn exec env
# go to project
# or create by -> yarn init -2
yarn set version stable
yarn set version from sources
yarn install
# if error
# remove yarn prefix on .zshrc
```
###### project
```sh
yarn add -D @vitejs/plugin-vue
yarn remove <package>
yarn outdated
yarn upgrade
yarn upgrade-interactive --latest
```
