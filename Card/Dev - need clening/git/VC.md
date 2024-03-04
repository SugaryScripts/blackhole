- [[#Advance|Advance]]
	- [[#Advance#Commit & add|Commit & add]]
	- [[#Advance#Git aliases|Git aliases]]
	- [[#Advance#Amend commit|Amend commit]]
- [[#Branch|Branch]]
	- [[#Branch#List Branch|List Branch]]
	- [[#Branch#Switch to a Branch That Came From a Remote Repo|Switch to a Branch That Came From a Remote Repo]]
	- [[#Branch#Merge a Branch|Merge a Branch]]
	- [[#Branch#Delete branch|Delete branch]]

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
##### Undo files
```sh
git checkout -- file

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
- checkout to the receiving branch
- make sure the branch is up to date `git fetch` then `git pull`
- Replace current branch with my-branch-name
`git merge -`
where `-` is the name of the branch that will be merged to the receiving branch
###### Delete branch
`git push origin --delete my-branch-name`
`git branch -d my-branch-name`

##### Remote
https://www.atlassian.com/git/tutorials/syncing/git-push

###### Push
```
checkout <branch>
push <remote> <branch>
```