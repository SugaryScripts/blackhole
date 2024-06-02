# General Use
```sh
npm ls -g --depth=0
npm i -g [package]
npm un [package]
```

>To list all the packages in your package directory
``` sh
npm list --depth 0 
```

>Use  to find out which of your npm dependencies are vulnerable.
```sh
npm audit
```

> list the packages that are out of date with respect to what is installed in package.json
```sh
npm outdated
npm -g outdated
```

> Use to update an individual package that has already been installed.
```sh
npm update package_name
```

> Use ~ and ~ to revert to a specific version.
```sh
npm uninstall package_name
npm install package_name@version
```

> Use  to clear npm's cache of all the packages that have been installed.
```sh
npm cache clean --force
```

# NPM npx react native
```sh
npx react-native start
npx react-native run-android
```