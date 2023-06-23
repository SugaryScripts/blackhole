[[Yarn]]

### Through nvm
pamac install nvm
sourcing zshrc
nvm install --lts
nvm install node
nvm install --latest-npm
nvm uninstall 18.14.0
nvm ls
npm -v
node -v
nvm -v
npm ls -g --depth=0
Use npm list --depth 0 to list all the packages in your package directory
Use npm audit to find out which of your npm dependencies are vulnerable.
Use npm outdated to list the packages that are out of date with respect to what is installed in package.json
Use npm update package_name to update an individual package that has already been installed.
Use npm uninstall package_name and npm install package_name@version to revert to a specific version.
Use npm cache clean --force to clear npm's cache of all the packages that have been installed.
npm update package

npx react-native start
npx react-native run-android