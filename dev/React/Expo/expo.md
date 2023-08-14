# Prerequisites

``` sh
yarn global add eas-cli
```


# New project expo
## Guide
### Create Project Expo Dev
#### New project
```sh
npm install --global eas-cli && \
npx create-expo-app expo-field && \
cd expo-field && \
eas init --id e797cafc-bbd2-4f75-b402-b80db93529d3
```
#### Link existing
```sh
npm install --global eas-cli && \
eas init --id e797cafc-bbd2-4f75-b402-b80db93529d3
```

## Create react native expo
```sh
yarn create expo-app expo-field
cd expo-field
eas init --id e797cafc-bbd2-4f75-b402-b80db93529d3
```
## Basic Package
```sh
yarn add typescript@4.9.4 @types/react@18.0.27 --dev
yarn add react-native-safe-area-context@4.5.0
yarn add react-native-screens
yarn add @react-navigation/native
yarn add @react-navigation/native-stack | stack
yarn expo install react-native-safe-area-context react-native-screens @react-navigation/native @react-navigation/native-stack
```
## Link github
```sh
eas build:configure
eas update configure

eas build --profile production
eas update --channel production
```
Update a production build:
1. Create a new build. Example: eas build --profile production.
2. Make changes in your project.
3. Publish an update. Example: eas update --channel production.
4. Force close and reopen the app at least twice to view the update.

Preview an update:
1. Publish an update to a branch. Example: eas update --branch new-feature.
2. In Expo Go or a development build, navigate to Projects > [project name] > Branch > Open.

https://docs.expo.dev/eas-update/github-actions/
>Add token from expo to github


# Dev build
> `eas build` will automatically create project if it doesn't exist yet
```sh
npx expo install expo-dev-client
eas login
eas json > "development": => "developmentClient": true,
eas build --profile development --platform android
npx expo start --dev-client
```
start production build
```sh
npx expo start --no-dev --minify
```

# Generate Keystore
```sh
keytool -genkey -v -keystore my-key.keystore -keyalg RSA -alias my-alias -sigalg SHA1withRSA -keysize 2048 -validity 10000
```
You will want to replace “my-release-key” with your name or company name for this key. For example, “gamesaladinc”. In the place of “alias_name”, you’ll create an alias for the key (only the first 8 characters are used), then hit enter.

```sh
turtle build:android --keystore-path my-key.keystore --keystore-alias my-alias
```

# Firebase

# Build Standalone !Uncontinued
## Android
- Build apk
```sh
expo build:android -t apk
```
- Android App Bundle for play store
```sh
expo build:android -t app-bundle
```
## Ios
```sh

```

## troubleshoot
```sh
npm i -g expo-cli@6.1.0
expo doctor --fix-dependencies
```

#### web build
```sh
npx expo export:web
npx serve web-build
```