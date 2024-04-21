up:: [[Ricing]] [[Linux]]
similar:: [[find]]


Search all
```sh
fzf
```

```sh
fzf -e
```
-e : exact matches only

Search and open it with vim
```sh
vim -o `fzf`
```

Search your history command
```sh
history | fzf +s --tac
```

Trigger fzf within command with `**`
In case forget the name files and don't want to back to file manager to search
```sh
vim ~/.config/** <TAB>
```

Changing the directory
```sh
cd /** <TAB>
```

Keybinding
- `Ctrl + T` : search 
- `Ctrl + R` : search command history
- `Alt + C`  | opt+c : change directory