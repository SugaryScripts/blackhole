## PyCharm Professional
2020.3 (LTS)

| version    | selorejo | sanders | main |     |
| ---------- | -------- | ------- | ---- | --- |
|            |          |         |      |     |
| 2023.1.6   | ✅        | ✅       | ✅    |     |
| 2023.2.3   |          |         |      |     |
| 2024.2 EAP | 🚧       | 🚧      |      |     |
| 2023.1.4   |          |         |      |     |
| 2023.1.5   |          |         |      |     |
| 2023.2.5   |          |         |      |     |
| 2023.3.5   |          |         |      |     |

## Php Storm
2021.1.4 (LTS)

| version    | selorejo | sanders | main | aiditech02 |
| ---------- | -------- | ------- | ---- | ---------- |
| 2022.1.4   | ✅        | ✅       | ✅    |            |
| 2022.2.5   | ✅        | ✅       | ✅    |            |
| 2022.3.3   |          |         | ✅    |            |
| 2023.1.4   |          |         | ✅    |            |
| 2023.2.3   |          |         | ✅    |            |
| 2023.3 EAP |          |         | ✅    |            |
| 2023.1.4   |          |         |      |            |
| 2023.1.5   | ✅        |         | ✅    |            |
| 2023.2.5   | ✅        | 🚧      |      |            |
| 2023.3.6   |          |         |      |            |


## laravel idea

| version | main | sanders |
| ------- | ---- | ------- |
| 0.7     | v    | v       |

# Plugins

| Category  | plugins                                           | PHP storm | Pycharm |
| --------- | ------------------------------------------------- | :-------: | :-----: |
| **Core**  | wakatime                                          |    ☑️     |   ☑️    |
|           | key promoter x                                    |    ☑️     |   ☑️    |
|           | .env                                              |           |         |
|           | php annotations                                   |    ☑️     |         |
|           | Php inspection (EA Extended)                      |    ☑️     |         |
|           | laravel plugin                                    |           |         |
|           | laravel tinker                                    |    ☑️     |         |
| **Theme** | rainbow brackets                                  |    ☑️     |   ☑️    |
|           | material theme ui                                 |           |         |
|           | material theme ui lite                            |           |         |
|           | atom material icon                                |           |         |
|           | doki icon                                         |    ☑️     |         |
|           | **doki theme** jetbrain \| Unthrottled            |    ☑️     |         |
|           | Noctumsempra's Color megapack                     |           |         |
|           | Catpuccin Themes                                  |           |         |
|           | Catpuccin Icons                                   |           |         |
|           | HardHacker Theme                                  |    ☑️     |         |
| **Misc**  | anime memes                                       |    ☑️     |         |
|           | Open Gitmoji                                      |    ☑️     |   ☑️    |
|           | gitmoji intellij                                  |           |         |
|           | gitmoji plus                                      |           |         |
|           | **background image plus** + \| HNUHell            |           |         |
|           | **theme randomizer** \| Unthrottled \| Alex Keith |           |         |
|           | Nyan progress \| Dmitry B                         |           |         |
## Best Themes
| plugin    | mode         | theme                 |
| --------- | ------------ | --------------------- |
| Catpuccin | light        | Latte                 |
|           | dark         | Mocha                 |
| Doki      | light        | Charlotte: Tomori Nao |
|           | dark         | Kanna                 |
|           |              | Gasai Yuno            |
|           | light & dark | Darkness              |
| Material  | dark         | Deep Ocean            |
 # FAQ
- Location config on linux sys


Misc
- Anime memes by Unthrottled
- Key Promoter X by Halirutan
- Github Markdown Emoji by Achim Seufert
- Gitmoji Plus: Commit Button by Patrice de Saint Steban
Dev
- Wakatime by WakaTime
- Laravel by Daniel Espendiller | Laravel tinker by Robbin
- .env files support by Adel F
- PHP Annotations by espend_de
Theme
- Doki Theme by Unthrottled
- Rainbow Brackets by izhangzhihao


# Settings
- node js
  go to Languages & Frameworks | Node. js
- Fonts -> Default; size:13 Lheight:1.2
  Editor | Font
  Editor | Color Scheme | Color Scheme Font

# Reset Eval version 2021
```sh
KEY=/home/$(whoami)/.config/JetBrains/*/eval/*.key;OTHER=/home/$(whoami)/.config/JetBrains/*/options/other.xml;PHPSTORM=/home/$(whoami)/.java/.userPrefs/jetbrains/phpstorm;WEBSTORM=/home/$(whoami)/.java/.userPrefs/jetbrains/webstorm;PYCHARM=/home/$(whoami)/.java/.userPrefs/jetbrains/pycharm;RIDER=/home/$(whoami)/.java/.userPrefs/jetbrains/rider;CLION=/home/$(whoami)/.java/.userPrefs/jetbrains/clion;DATALORE=/home/$(whoami)/.java/.userPrefs/jetbrains/datalore;DATAGRIP=/home/$(whoami)/.java/.userPrefs/jetbrains/datagrip;RUBYMINE=/home/$(whoami)/.java/.userPrefs/jetbrains/rubymine;APPCODE=/home/$(whoami)/.java/.userPrefs/jetbrains/appcode;GOLAND=/home/$(whoami)/.java/.userPrefs/jetbrains/goland;rm -f $KEY $OTHER;rm -rf $PHPSTORM $WEBSTORM $PYCHARM $RIDER $CLION $DATALORE $DATAGRIP $RUBYMINE $APPCODE $GOLAND;echo "processing: find existing file, please wait ...";echo "processing: delete existing eval key ...";echo "processing: file deleted.";echo "done: success reseting your Jerbrains IDE.";
```


windows
[JetBrains IDE trial reset windows · GitHub](https://gist.github.com/rjescobar/4b7200d7b2274c029107ca8b9d02f3a3)
```bat
REM Delete eval folder with licence key and options.xml which contains a reference to it
for %%I in ("WebStorm", "IntelliJ", "CLion", "Rider", "GoLand", "PhpStorm", "Resharper", "PyCharm") do (
    for /d %%a in ("%USERPROFILE%\.%%I*") do (
        rd /s /q "%%a/config/eval"
        del /q "%%a\config\options\other.xml"
    )
)

REM Delete registry key and jetbrains folder (not sure if needet but however)
rmdir /s /q "%APPDATA%\JetBrains"
reg delete "HKEY_CURRENT_USER\Software\JavaSoft" /f
```