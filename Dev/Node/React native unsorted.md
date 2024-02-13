react native

## Source
# progress
https://www.npmjs.com/package/react-native-progress

# React scroll listview using button
https://snack.expo.dev/embedded/@aboutreact/react-native-scroll-up-or-down-the-listview-on-the-click-of-button-?platform=web
https://spin.atomicobject.com/2021/04/20/react-native-building-scroll-top-button/
# timer component
https://community.draftbit.com/c/code-snippets/timer-component-using-screen-variables-and-custom-function
# extract key path troubleshooting
https://community.draftbit.com/c/help/extract-key-path-troubleshooting
# Shuffle javascript array
https://www.webmound.com/shuffle-javascript-array/
# loading spinner
https://community.draftbit.com/c/help/how-to-add-screen-loader-spinner-while-data-is-loading
# time
https://community.draftbit.com/c/code-snippets/add-relative-timestamps-to-your-app-with-momentjs-and-low-code
# Pull refresh list
https://blog.expo.dev/react-native-pull-to-refresh-make-refreshing-easy-for-users-813088732c4f
# fetch data in custom component
https://community.draftbit.com/c/code-snippets/fetching-data-in-custom-component
# html rich text
https://medium.com/@nutanbhogendrasharma/how-to-display-html-content-in-react-native-mobile-app-b43cfda8325

make sure don't use sudo for anything
https://medium.com/@ExplosionPills/dont-use-sudo-with-npm-5711d2726aa3
npm uninstall -g yarn

deprecated tar@2.2.2: This version of tar is no longer supported,
npm i tar

sudo pacman -S nodejs npm
npm install yarn -g
npm install -g create-react-app
or
yarn global add create-react-app

craete
create-react-app hello-world
cd hello-world
npm start
or yarn start







# check updates of npm package
https://medium.com/subjective-developer/update-all-node-packages-to-latest-aa128396b92b
# newer version of npm
https://stackoverflow.com/questions/9755841/how-can-i-change-the-version-of-npm-using-nvm#:~:text=on%20this%20post.-,nvm%20now%20has%20a%20command%20to%20update%20npm.,npm%20install%20%2D%2Dlatest%2Dnpm%20.
# safe update npm
https://josipmisko.com/posts/how-to-update-npm-packages-in-4-easy-steps
# unable to resolve npm install
https://weekendprojects.dev/posts/fix-for-npm-conflicting-peer-dependency-error/
https://stackoverflow.com/questions/71835697/create-react-app-dependency-version-issues-with-react-18




# react native project
https://www.interviewbit.com/blog/react-native-projects/



You need to source nvm before you can use it. Do one of the following
or similar depending on your shell (and then restart your shell):

  echo 'source /usr/share/nvm/init-nvm.sh' >> ~/.bashrc
  echo 'source /usr/share/nvm/init-nvm.sh' >> ~/.zshrc

You can now install node.js versions (e.g. nvm install 10) and
activate them (e.g. nvm use 10).

init-nvm.sh is a convenience script which does the following:

[ -z "$NVM_DIR" ] && export NVM_DIR="$HOME/.nvm"
source /usr/share/nvm/nvm.sh
source /usr/share/nvm/bash_completion
source /usr/share/nvm/install-nvm-exec

You may wish to customize and put these lines directly in your
.bashrc (or similar) if, for example, you would like an NVM_DIR
other than ~/.nvm or you don't want bash completion.

See the nvm readme for more information: https://github.com/creationix/nvm

:: Running post-transaction hooks...
(1/1) Arming ConditionNeedsUpdate...



===========Linux Users PLEASE README FIRST ===========
If you found issue when click on the "Debug Android" button, error message: 
 "SDK location not found ", or Task 'installDebug' not found in project ':app',
 please fix it like this :
add a android local config file:
yourapp/android/local.properties
sdk.dir=/Users/xxxx/Documents/Java/android-sdk-macosx
let sdk.dir point to your ANDROID_HOME environment 
if can't find adb, try this shell command:
sudo ln -s ~/Android/Sdk/platform-tools/adb /usr/bin/adb
If can't find avd list, try this shell command(please ensure your emulator path):
sudo ln -s /Users/my_user/Library/Android/sdk/emulator /usr/bin/emulator
More info please ref this issue:
https://github.com/beansoftapp/react-native-console/issues/17


https://stackoverflow.com/questions/23556330/run-nvm-use-automatically-every-time-theres-a-nvmrc-file-on-the-directory


https://stackoverflow.com/questions/62936608/how-do-i-stop-expo-from-running-in-the-web
https://www.npmjs.com/package/n
https://stackoverflow.com/questions/51580180/react-native-bundling-failed-unable-to-resolve-module-accessibilityinfo
https://stackoverflow.com/questions/71835697/create-react-app-dependency-version-issues-with-react-18
https://stackoverflow.com/questions/31472755/sudo-npm-command-not-found
# flatlist fix
https://javascript.plainenglish.io/how-to-fix-virtualizedlists-should-never-be-nested-inside-plain-scrollviews-warning-3a2a887b4ea0
# use state 
https://www.pluralsight.com/guides/fetching-data-updating-state-hooks


onTextChange(function_name)
    - calling with parenthesis () will execute those functions before the render is done
    - without (), will be called when the text changed || ideal choice


npm i -g npm-check-updates
ncu => ncu -u => npm install


build expo || deploy
https://docs.expo.dev/build/setup/#prerequisites


# dynamic
## page
id, name, description
## question
id, text, type, navigation
## responses
id, page_id
## answers
id, page_id, question_id, answer



# npx expo
## Install
npx create-expo-app [app name]
yarn create expo-app
pnpm create expo-app
## Web
npx expo install react-dom react-native-web @expo/webpack-config
npx expo start

## Init apps


## Fresh init project
yarn global add eas-cli
yarn create expo-app measure-location
cd measure-location
eas init --id 85c66031-88bf-4315-92a5-1452fe1dad69

## Existing codebase
npm install --global eas-cli
eas init --id 85c66031-88bf-4315-92a5-1452fe1dad69


## Eas
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
eas channel:delete master


All builds of your app going forward will be eligible to receive updates published with EAS Update.

EAS Build is not configured. If you'd like to use EAS Build with EAS Update, run eas build:configure, then re-run eas update:configure to configure eas.json with EAS Update.

🎉 Your app is configured with EAS Update!

Next steps:

Update a production build:
1. Create a new build. Example: eas build --profile production.
2. Make changes in your project.
3. Publish an update. Example: eas update --channel production.
4. Force close and reopen the app at least twice to view the update.

Preview an update:
1. Publish an update to a branch. Example: eas update --branch new-feature.
2. In Expo Go or a development build, navigate to Projects > [project name] > Branch > Open.


# Development build
npx expo install expo-dev-client
eas login
eas json > "development": => "developmentClient": true,
eas build --profile development --platform android
npx expo start --dev-client
npx expo start --no-dev --minify


typescript @types/react --dev

react-native-safe-area-context
react-native-screens
@react-navigation/native
@react-navigation/native-stack


# Main expo-field
## Tutor
### new project
npm install --global eas-cli && \
npx create-expo-app expo-field && \
cd expo-field && \
eas init --id e797cafc-bbd2-4f75-b402-b80db93529d3
### Link existing
npm install --global eas-cli && \
eas init --id e797cafc-bbd2-4f75-b402-b80db93529d3