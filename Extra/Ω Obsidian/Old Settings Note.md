#deprecated


# Plugin
```
Obsidian Git
Emoji Shortcode
Obsidian Git
```
# gitignore
>edit with external editor
```json
# to exclude Obsidian workspace settings (including plugin and hotkey configurations)
.obsidian/*

# OR only to exclude workspace cache
.obsidian/workspace/*

# Exclude plugins
.obsidian/plugins/*

# Exclude consultant specific files "personal"
05*-*Personal/

# Exclude Day Planner directory placed in vault root
Day*Planners/*

# This file is used to keep track of last auto backup/pull
.obsidian-git-data

# Exclude Untitled Notes
Untitled*
# Exclude "bad" names
null*

# Add below lines to exclude OS settings and caches
.trash/
.DS_Store
```

# Preference
```json
preferences [
	default-new-file: 'same folder',
	default-loc-attachment: 'same folder',
	permanently delete
	hotkeys-header ctrl-shift-.
]
themes=blue topaz
core [
	git
]
community [
	
]
```
> put community plugins here
```json
[
  "obsidian-git",
  "table-editor-obsidian",
  "automatic-table-of-contents",
  "obsidian-wakatime",
  "waka_time_box"
]
```

