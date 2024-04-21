similar:: [[Vim]] || [[Vim Tutorial]]

# Case
## Write as Root / Sudo
url:: [How does the vim "write with sudo" trick work? - Stack Overflow](https://stackoverflow.com/questions/2600783/how-does-the-vim-write-with-sudo-trick-work)
```vim
:w !sudo tee %
```
- `%` : the current file name
- `w` : save
	- `w test2.txt`  : save as new file name
- tee ???
