tags:: #vc/git 
up:: [[Terminal]] [[Git]]

```sh
which ssh-askpass

pacman -Ss ssh-askpass
pacman -S ksshaskpass

rm /usr/lib/ssh/ssh-askpass
ln /usr/bin/ksshaskpass /usr/lib/ssh/ssh-askpass
```

pass kwallet -> blowfish = root pass

revert
```sh
rm /usr/lib/ssh/ssh-askpass
ln /usr/lib/ssh/x11-ssh-askpass /usr/lib/ssh/ssh-askpass
```