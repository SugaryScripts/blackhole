up:: [[Git]]

# Commit

#### GCAM
```sh
git commit --all --message "<message>"
```
- **--all** : Automatically tracked all modified, deleted, added files
- **--message** "message": specifies the actual commit message

#### GCAN!

```sh
git commit --verbose --all --signoff --no-edit --amend
```
- **--verbose** : show the exact changes or diff on each files
- **--signoff** : add your name on git commit message detail (for open source)
