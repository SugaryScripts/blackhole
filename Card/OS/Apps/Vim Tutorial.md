similar:: [[Vim]] || [[Vim Command]]

### Text Editing
- Lesson 1
	- press `x` to delete character
	- press `i` to insert mode
		- Type text before the cursor
	- press `A` to append
		- Type text at the end of the current line
- Lesson 2
	- type `dw` to delete a word
	- `d$` to delete to the end of the line
	- Operator and Motion -> `d[motion]` -> `d` is delete operator
	  Short list of motion
		- `w` = until the start of the **next word**
		- `e` = to the end of the **current word**
		- `$` = to the end of the **line**
	- Using count cursor
		- `2w`  = move the cursor **2nd** words forward
		- `3e` = cursor to the **end of 3rd** words forward
	- Delete with count
		- `d2w` = delete 2 word
		- `dd` = delete a line
		- `2dd` = delete 2 line
	- `U` = undo all change
	- `u` = undo previous change
	- `C-R` = redo
- Lesson 4
	- `/` = search -> `n` next, `N` previous -> `:set hlsearch` to highlight it
- Lesson 6
	- `y` to copy/yank & `p` to paste
