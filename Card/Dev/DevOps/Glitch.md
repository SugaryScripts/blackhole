##### Disk Full
[Disk Space Warning – Glitch](https://help.glitch.com/hc/en-us/articles/16287552960269-Disk-Space-Warning)
- Check disk space using `$ df`
- Run `git gc` and `git prune`, this will help cleanup files and remove unreachable objects
- If you’re not worried about git history, remove the `.git` folder using `$ rm -rf .git`
- Remove unused dependencies from your `package.json`
- Review your dependencies in the `node_modules` folder.
```sh
rm -rf .git .node_modules .local .cache
```

###### EOL Python 3.7
[Upgrade Python version from 3.7 (which is now EOL) to something more recent? - Glitch Feature Ideas - Glitch Community Forum](https://support.glitch.com/t/upgrade-python-version-from-3-7-which-is-now-eol-to-something-more-recent/63011/3)
[Glitch :･ﾟ✧](https://glitch.com/edit/#!/narflinger-python-310?path=server.py%3A24%3A0)
[NAR Flinger, a package installer in a single script - The Gallery - Glitch Community Forum](https://support.glitch.com/t/nar-flinger-a-package-installer-in-a-single-script/62276/6)
