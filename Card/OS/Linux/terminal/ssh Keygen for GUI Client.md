tags:: #vc/git 
up:: [[Linux]] [[Atlas/Git]]

##### Plasma
[^ln]
```sh
which ssh-askpass

pacman -Ss ssh-askpass
pacman -S ksshaskpass

rm /usr/lib/ssh/ssh-askpass
ln -sf /usr/bin/ksshaskpass /usr/lib/ssh/ssh-askpass
```

pass kwallet -> blowfish = root pass

revert
```sh
rm /usr/lib/ssh/ssh-askpass
ln -sf /usr/lib/ssh/x11-ssh-askpass /usr/lib/ssh/ssh-askpass
```

###### Reset kwallet
Delete `/home/fryctze/.local/share/kwalletd`

##### Seahorse
Condition case at the time: x11-ssh-askpass is not installed yet [^ln]
```sh
ls /usr/lib/seahorse
ls /usr/lib/ssh
ln -s /usr/lib/seahorse/ssh-askpass /usr/lib/ssh/ssh-askpass
```



[^ln]: [[ln - Symbolic Links]]