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