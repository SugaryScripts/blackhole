up:: [[Linux]]
url:: [Home · polybar/polybar Wiki · GitHub](https://github.com/polybar/polybar/wiki)
integration:: [[Pywal]]

# Installation
1. Create config
   by copying the default config to become yours
```sh
mkdir ~/.config/polybar
cp /etc/polybar/config.ini ~/.config/polybar/config.ini
polybar example
```
2. Make launch.sh for startup
```sh
cd ~/.config/polybar
touch launch.sh
chmod +x launch.sh
vim launch.sh
```
Paste this
```sh
#!/usr/bin/env bash

# Terminate already running bar instances
# If all your bars have ipc enabled, you can use 
polybar-msg cmd quit
# Otherwise you can use the nuclear option:
# killall -q polybar

# Launch bar1 and bar2
# echo "---" | tee -a /tmp/polybar1.log /tmp/polybar2.log
echo "---" | tee -a /tmp/polybar1.log
polybar bar1 2>&1 | tee -a /tmp/polybar1.log & disown
# polybar bar2 2>&1 | tee -a /tmp/polybar2.log & disown

echo "Bars launched..."
```
- `bar1` & `bar2` is the names of the bar in `config.ini`

3. Setup auto start i3 config
```json
exec_always ~/.config/polybar/launch.sh
```

# Config Customization
[Configuration · polybar/polybar Wiki · GitHub](https://github.com/polybar/polybar/wiki/Configuration#bar-settings)

