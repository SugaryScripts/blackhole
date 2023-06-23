#### Basic

```sh
yarn add -D eslint eslint-config-prettier eslint-config-universe eslint-plugin-react-hooks
```

##### typescript
```sh
yarn add -D install @types/react @types/react-native typescript
```
###### tsconfig.json
```json
{
  "extends": "expo/tsconfig.base",
  "compilerOptions": {
    "strict": true
  }
}
```

##### prettier
`yarn add -D prettier`

###### .prettierrc.json
```json
{
  "arrowParens": "avoid",
  "bracketSpacing": true,
  "bracketSameLine": true,
  "printWidth": 80,
  "semi": true,
  "singleQuote": true,
  "tabWidth": 2,
  "trailingComma": "all",
  "useTabs": false
}
```

##### .eslintrc.js
```json
module.exports = {  
  env: {  
    browser: true,  
    es2021: true,  
    node: true,  
  },  
  extends: ['universe', 'plugin:react-hooks/recommended', 'prettier'],  
  parser: '@typescript-eslint/parser',  
  parserOptions: {  
    ecmaVersion: 'latest',  
    sourceType: 'module',  
  },  
  plugins: ['react', 'prettier'],  
  settings: {  
    react: {  
      version: 'detect',  
    },  },  
  rules: {},  
};
```

##### Script for package.json
```json
script {
"test:eslint": "echo \"\\033[33mRunning eslint check\" &&  eslint .",
"test:tsc": "echo \"\\033[33mRunning typescript check\" && tsc"
}
```
```json
"lint:fix": "eslint --fix 'src/**/*.{js,jsx,ts,tsx,json}'",  
"format": "prettier --write 'src/**/*.{js,jsx,ts,tsx,css,md,json}' --config ./.prettierrc"
```


Source
https://www.headway.io/blog/react-native-quick-start-expo-eslint-typescript-and-prettier


#### Unifinished
```sh
yarn add -D eslint
yarn eslint --init

✔ How would you like to use ESLint? · style
✔ What type of modules does your project use? · esm
✔ Which framework does your project use? · react
✔ Does your project use TypeScript? · No / Yes
✔ Where does your code run? · browser, node
✔ How would you like to define a style for your project? · guide
✔ Which style guide do you want to follow? · standard-with-typescript
✔ What format do you want your config file to be in? · JavaScript

```