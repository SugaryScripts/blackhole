up:: [[Home]]
url:: [GitHub - termux/termux-app: Termux - a terminal emulator application for Android OS extendible by variety of packages.](https://github.com/termux/termux-app#installation)

### Setup
1. Setup storage
[0% \[working\]: · Issue #15357 · termux/termux-packages · GitHub](https://github.com/termux/termux-packages/issues/15357)
`pkg install -y openssl`
```sh
termux-change-repo
yes | pkg upgrade
pkg upgrade
termux-setup-storage
```
Create symlink to android storage to be accessible via termux terminal
2. Git
> `pkg` is recommended
```sh
apt upgrade && apt update
pkg install openssl-tool
pkg install openssh git

ssh-keygen -t ed25519 -C "a12@NEKO-chan"
git config --global user.email "fikryfarenza@gmail.com"
git config --global user.name "Farenza"


ln -s /storage/emulated/0/Documents/blackhole ~/blackhole
```

### Package Command
url:: [Package Management - Termux Wiki](https://wiki.termux.com/wiki/Package_Management)

| Command                   | Description                                |
| ------------------------- | ------------------------------------------ |
| `pkg autoclean`           | Remove outdated .deb files from the cache. |
| `pkg clean`               | Remove all .deb files from the cache.      |
| `pkg files <package>`     | List files installed by specified package. |
| `pkg list-all`            | List all available packages.               |
| `pkg list-installed`      | List currently installed packages.         |
| `pkg reinstall <package>` | Re-install specified package.              |
| `pkg search <query>`      | Search package by query.                   |
| `pkg show <package>`      | Show information about specific package.   |
| `apt list --upgradable`   |                                            |
### Troubleshoot
