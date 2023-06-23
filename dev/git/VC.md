##### Advance
###### Commit & add
```sh
git commit -am "Easy add & commit"
```
###### Git aliases
```sh
git config --global alias.ac "commit -am"
git am "noice!"
```
###### Amend commit
```sh
git add .
git commit --amend -m "Nice!"
git commit --amend --no-edit
```

##### Branch

###### List Branch
- local
	`git branch`
- remote
	`git branch -r`
- all
	`git branch -a`

###### Switch to a Branch That Came From a Remote Repo
- get a list of all branches from the remote
	`git pull`
- Switch
	`git checkout --track origin/my-branch-name`

###### Merge a Branch
Replace current branch with my-branch-name
`git merge my-branch-name`

###### Delete branch
`git push origin --delete my-branch-name`
`git branch -d my-branch-name`
