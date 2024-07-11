```sh
termux-setup-storage
pkg update && pkg upgrade
pkg install git
pkg install gh

# Login to github account
gh auth login
git config --global user.name "name"
git config --global user.email "email"

# Sync script
mkdir -p /data/data/com.termux/files/home/.shortcuts
chmod 700 -R /data/data/com.termux/files/home/.shortcuts
mkdir -p /data/data/com.termux/files/home/.shortcuts/tasks
chmod 700 -R /data/data/com.termux/files/home/.shortcuts/tasks
nano /data/data/com.termux/files/home/.shortcuts/tasks/sync_script.sh

#!/bin/bash
cd storage/shared/LifeWiki
git pull && git add -A && git commit -a -m "android vault backup: `date +'%Y-%m-%d %H-%M-%S'`"
git push
```