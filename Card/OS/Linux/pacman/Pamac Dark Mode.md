url:: [Pamac not dark after update - Support - Manjaro Linux Forum](https://forum.manjaro.org/t/pamac-not-dark-after-update/144112)

pro:
- The theme are sync with manjaro theme (customize look & feel)
cons:
- For each loading, took so much time
- Not responding might happen

##### Install gtk for dark mode support
```sh
sudo pacman -R pamac-gtk && sudo pacman -S pamac-gtk3
```


If failed then, try this:
```sh
sudo pacman -Rdd pamac-gtk && sudo pacman -S pamac-gtk3
```

##### Revert it back to light
```sh
sudo pacman -R pamac-gtk3 && sudo pacman -S pamac-gtk
```