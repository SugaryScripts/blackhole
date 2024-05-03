up:: [[Home]]
# Case
#### Ignore on specific domain
url:: [disable tridactyl on some sites · Issue #587 · tridactyl/tridactyl · GitHub](https://github.com/tridactyl/tridactyl/issues/587)
Ignore a site
```sh
autocmd DocStart YOUR_DOMAIN mode ignore
```
Enable it back
```sh
autocmddelete DocStart YOUR_DOMAIN mode ignore
```
typing.com
youtube.com
# Cheatsheet
C = Ctrl

### Hint mode

|                                                     |                       |
| --------------------------------------------------- | --------------------- |
| Note : Hint characters should be typed in lowercase |                       |
| Semicolon can be replaced by the command "­:hint -" |                       |
|                                                     |                       |
| Enter Hint mode                                     | f                     |
| Open link in background tab                         | F                     |
| **Extented hint mode**                              |                       |
| Open image in curren­t/new tab                      | ;i/;I                 |
| Save/ Save-as the linked source                     | ;s/;a                 |
| Save / Save-as the select image                     | ;S/;A                 |
| Copy an element's text to the clipboard             | ;p                    |
| copy an element's title/alt text to the clipboard   | ;P                    |
| copy an element's link URL to the clipboard         | ;y                    |
| copy an element's anchor URL to the clipboard       | ;#                    |
| read the element's text with text-t­o-s­peech       | ;r                    |
| Kill an element of the page                         | ;k                    |
| Kill an element (can be restored)                   | ;K (:elem­ent­unhide) |
| focus an element                                    | ;;                    |
### Navigating current page

| Navigate Page                               |                |
| ------------------------------------------- | -------------- |
| Scroll up/down                              | j/k            |
| Scroll left/right                           | h/l            |
| Scroll to top/bottom of page                | gg/G           |
| Reload­/Hard reload                         | r/R            |
| Focus the last-used input on page           | gi             |
| Copy URL page to clipboard                  | yy             |
| Go to parent of current URL                 | gu             |
| Go to root domain of current URL            | gU             |
| Zoom in/Zoom out/De­fault                   | zi/zo/zz       |
| Jump to the next/p­revious part of the page | <C-­f>/­<C-­b> |
|                                             |                |
|                                             |                |

### Navigating tabs

|   |   |
|---|---|
|Close current tab|d|
|Reopen last tab (or window) closed|u|
|Go to next/p­revious tab|gt/gT|
|List tabs|b (Tab/T­ab-­Shirt to navigate list)|
|Go to first/last tab|g^ OR g0/g$|
|Go to tab playing audio|ga|
|Go to last active tab|g^|


### Navigate to new pages

|                                             |                             |
| ------------------------------------------- | --------------------------- |
| Open URL in current tab                     | o/O (pre-loads current URL) |
| Open URL in new tab                         | t/T (pre-loads current URL) |
| Open URL in new window                      | w/W (pre-loads current URL) |
| Opens clipboard content in curren­t/new tab | p/P                         |
| Engine search in curren­t/new tab           | s/S                         |
| Go to pages set with "set home [url1]..."­  |                             |
### Visual mode

|   |   |
|---|---|
|Activate|v|
||Mouse select|
||/ (search results)|
|**Visual mode keybinds**|   |
|Expand­/reduce by 1 char|h/l|
|To end of line|$|
|To begining of line|0|
|Expand to next/p­revious word|e/b|
|Expand to next/p­revious line|j/k|
|Expand progre­ssively to whole page|=|
|Search for selection|s/S|
|Yank to clipboard|y|

### General commands

|                              |               |
| ---------------------------- | ------------- |
| Activate command line        | :             |
| Enable­/di­sable ignore mode | Shift+­Insert |
| Repeat last command          | .             |
| Hint mode                    | f             |
| Visual mode                  | v             |
| Bypass bindings              | <C-­v>        |

# Settings
url:: [How to access configuration? · Issue #3502 · tridactyl/tridactyl · GitHub](https://github.com/tridactyl/tridactyl/issues/3502)

`:help set`

Smooth scroll
`:set smoothscroll true`



# Mode
- Normal mode
    - This mode is used for navigating around single pages and starting other modes.
    - Tabs are usually in this mode. You can enter normal mode from the other modes by pressing `Escape`.
- Hint mode - `f`
    - This mode **highlights** elements on the web page **and performs actions** on those elements.
    - This is most often used for following links, but it has many other submodes.
    - You can enter this mode with `f` and exit it with `Escape` or `Ctrl-[`.
    - Hint characters are displayed as uppercase letters, **but you should type the lowercase letter**.
- Visual mode (experimental) - `v`
    - This mode allows you to **select text** on the web page and **copy** it to the **clipboard or search** for it using `s` and `S`.
    - You can enter this mode with `v`, by selecting text with the mouse, `;h` hint mode, `/` searching or by using Firefox's "caret" mode on `F7` and exit it with `Escape` or `Ctrl-[`.
- Command mode ("ex-mode") - `:`
    - This mode allows you to execute more complicated commands by typing them out manually.
    - It is commonly used for binding keys and accessing help.
    - You can enter this mode with `:` and exit it with `Escape` or `Enter`.
- Ignore mode
    - This mode passes all keypresses through to the web page. It is useful for websites that have their own keybinds, such as **games and Gmail**.
    - You can toggle the mode with `Shift-Insert`, `Ctrl-Alt-Escape`, `Ctrl-Alt-Backtick`, or `Shift-Esc`.
    - While in ignore mode, you can execute a single normal mode binding by pressing `<C-o>` followed by the keys for the binding.
    - While in normal mode, you can enter ignore mode for one keypress / key combination by pressing `<C-v>`.
    - Tridactyl can be configured to enter ignore mode for specified URLs. Run `:blacklistadd [url]` to put Tridactyl in ignore mode on the provided URL. Use the command `:blacklistremove [url]` to remove the URL from the blacklist.