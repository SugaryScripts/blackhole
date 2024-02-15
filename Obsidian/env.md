
```table-of-contents
style: nestedList # TOC style (nestedList|inlineFirstLevel)
minLevel: 0 # Include headings from the specified level
maxLevel: 0 # Include headings up to the specified level
includeLinks: true # Make headings clickable
debugInConsole: false # Print debug info in Obsidian console
```
# wakatime
Copy it from https://wakapi.dev/summary instead wakatime. Because it already sync (wakapi read/write wakatime) (wakatime can't read/write into wakapi)
# gitignore
```json
# to exclude Obsidian workspace settings (including plugin and hotkey configurations)
.obsidian/*
.obsidian/workspace.json

# Exclude others
!.obsidian/app.json
!.obsidian/appearance.json
!.obsidian/community-plugins.json
!.obsidian/core-plugins.json
!.obsidian/core-plugins-migration.json
!.obsidian/graph.json
!.obsidian/hotkeys.json

# Add below lines to exclude OS settings and caches
.trash/
```