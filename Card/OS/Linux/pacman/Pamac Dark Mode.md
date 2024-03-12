url:: [Pamac not dark after update - Support - Manjaro Linux Forum](https://forum.manjaro.org/t/pamac-not-dark-after-update/144112)

```sh
sudo pacman -R pamac-gtk && sudo pacman -S pamac-gtk3
```


If failed then, try this:
```sh
sudo pacman -Rdd pamac-gtk && sudo pacman -S pamac-gtk3
```