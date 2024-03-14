
url:: [Pamac - Manjaro](https://wiki.manjaro.org/index.php/Pamac)


## Updating the System

To check if updates are available, you can use the command:

```sh
user $ pamac checkupdates -a
```
  
To update all installed packages installed from the repos or [AUR](https://wiki.manjaro.org/index.php/Arch_User_Repository "Arch User Repository"), you can use the command:

```sh
user $ pamac upgrade -a
```

## Dealing with Orphaned Packages

To check to see if there any orphaned packages (packages which are no longer needed) installed, you can use:

```sh
user $ pamac list -o
```

To remove all orphans use the command:

```sh
user $ pamac remove -o
```
## Cleaning the Cache

When pamac installs packages, it keeps a copy of all the old packages you have downloaded. This cache can be very useful if you have to install older packages in an emergency. However, left unchecked, this cache will grow very large over time.

Otherwise, to clear the cache completely, enter the following command (and use with care):

```sh
user $ pamac clean
```

A safer way to remove old package cache files is to remove all packages except for the latest three package versions using:

```sh
user $ pamac clean --keep 3
```