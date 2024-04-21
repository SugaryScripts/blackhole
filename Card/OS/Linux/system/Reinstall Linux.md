up:: [[Home]] [[Linux]]

Frequent Commands
```sh
sudo mount -t ntfs /dev/sda3 ~/Documents/mnt
```

- Backup
	- Check **Sublime** notes
	- Commit = push projects
	- Blackholes notes
	- Jetbrains plugin
	- **Waka** Token / Config
	- Push **dotfiles**
	- **ssh**
	- Export Browser tabs - history - bookmaks (tab url into notes?)
	- History zsh
	- video screenshots, swr plugins
	- Databases Development
	- Ignored Git Repo
		- Obsidian Git settings json

ssh
```
╰─ ls -al                                                                                                                           ─╯
total 40
drwx------  2 fryctze fryctze 4096 Feb 20 23:17 .
drwx------ 50 fryctze fryctze 4096 Apr  4 03:06 ..
-rwx------  1 fryctze fryctze  578 Apr  3 01:03 config
-rw-------  1 fryctze fryctze 2602 Jan 16 23:30 google_compute_engine
-rw-r--r--  1 fryctze fryctze  569 Jan 16 23:30 google_compute_engine.pub
-rw-r--r--  1 fryctze fryctze  109 Jan 16 23:30 google_compute_known_hosts
-rwx------  1 fryctze fryctze 1112 Feb 20 22:56 known_hosts
-rwx------  1 fryctze fryctze  748 Sep  6 2022 known_hosts.old
-rw-------  1 fryctze fryctze  464 Sep 22 2021 me
-rw-------  1 fryctze fryctze   97 Sep 22 2021 me.pub
╭─    ~/.ssh ▓▒░··································
```

- New
	- fryctze AI-chan
	- pass on next warden


# Starting New

### Fonts
```sh
adobe-source-han-sans- cn | jp | kr | -fonts , ttf-joypixels

sudo pacman -S adobe-source-han-sans- cn-fonts adobe-source-han-sans-jp-fonts adobe-source-han-sans-kr-fonts ttf-joypixels
```

### Dates
```sh
timedatectl status
timedatectl set-ntp true
timedatectl list-timezones
timedatectl set-timezone Asia/Jakarta
```

### Java
```sh
archlinux-java set $java_env
```


### Node JS
[[N]]


## Minor Troubleshoot
### Error install_pulse
Remove pa-applet on `/usr/bin/install_pulse` and on `.i3/config`
```sh
sudo pacman -Sy manjaro-pulse pavucontrol || exit 1
```