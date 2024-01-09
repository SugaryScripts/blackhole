
source 
https://forum.manjaro.org/t/gpg-packet-with-unknown-version-252/137065/8

pacman-key --init  
pacman-key --populate  
pacman-key --refresh-keys  
pacman -Sy archlinux-keyring

clean corrupted database
```
pacman -Scc
```

###### 1
[[#2]]
```sh
sudo rm -r /etc/pacman.d/gnupg
sudo pacman-key --init

gpg: /etc/pacman.d/gnupg/trustdb.gpg: trustdb created
gpg: no ultimately trusted keys found
gpg: starting migration from earlier GnuPG versions
gpg: porting secret keys from '/etc/pacman.d/gnupg/secring.gpg' to gpg-agent
gpg: migration succeeded
==> Generating pacman master key. This may take some time.
gpg: Generating pacman keyring master key...
gpg: directory '/etc/pacman.d/gnupg/openpgp-revocs.d' created
gpg: revocation certificate stored as '/etc/pacman.d/gnupg/openpgp-revocs.d/3E2A5ED4B4691CA684C62EC7F1CCE03270499482.rev'
gpg: Done
==> Updating trust database...
gpg: marginals needed: 3  completes needed: 1  trust model: pgp
gpg: depth: 0  valid:   1  signed:   0  trust: 0-, 0q, 0n, 0m, 0f, 1u
```

###### 2
[[#3]]
```sh
sudo pacman-key --populate archlinux manjaro

==> Appending keys from archlinux.gpg...
==> Appending keys from manjaro.gpg...
gpg: error reading key: No public key
gpg: error reading key: No public key
gpg: error reading key: No public key
gpg: error reading key: No public key
gpg: error reading key: No public key
gpg: error reading key: No public key
gpg: error reading key: No public key
gpg: error reading key: No public key
==> Locally signing trusted keys in keyring...
  -> Locally signed 23 keys.
==> Importing owner trust values...
gpg: setting ownertrust to 4
gpg: setting ownertrust to 4
gpg: setting ownertrust to 4
gpg: inserting ownertrust of 4
gpg: setting ownertrust to 4
gpg: inserting ownertrust of 4
gpg: setting ownertrust to 4
gpg: setting ownertrust to 4
gpg: setting ownertrust to 4
```

###### 3
[[#4]]
```sh
sudo pacman -Sy gnupg archlinux-keyring manjaro-keyring

:: Synchronizing package databases...
 core is up to date
 extra is up to date
 community is up to date
 multilib is up to date
warning: gnupg-2.2.41-1 is up to date -- reinstalling
warning: archlinux-keyring-20230320-1 is up to date -- reinstalling
warning: manjaro-keyring-20230318-1 is up to date -- reinstalling
resolving dependencies...
looking for conflicting packages...

Packages (3) archlinux-keyring-20230320-1  gnupg-2.2.41-1  manjaro-keyring-20230318-1

Total Installed Size:  10,88 MiB
Net Upgrade Size:       0,00 MiB

:: Proceed with installation? [Y/n] y
(3/3) checking keys in keyring                                                                                                                                             [----------------------------------------------------------------------------------------------------------] 100%
(3/3) checking package integrity                                                                                                                                           [----------------------------------------------------------------------------------------------------------] 100%
(3/3) loading package files                                                                                                                                                [----------------------------------------------------------------------------------------------------------] 100%
(3/3) checking for file conflicts                                                                                                                                          [----------------------------------------------------------------------------------------------------------] 100%
(3/3) checking available disk space                                                                                                                                        [----------------------------------------------------------------------------------------------------------] 100%
:: Processing package changes...
```


###### 4
```lua
sudo pacman -Syyu
```

``` sh
sudo pacman -Fyy
```