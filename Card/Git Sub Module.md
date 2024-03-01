> Its Nested Repository

up:: 
tags:: #git

# What
- It's **like a package manager** but it's git. 
- **Independent** entities within a parent repository
	- **changes** are saved **different** from the parent
		- Each changes on sub must be **committed within that sub** only
		- Changes on parent must be **committed on root folder** parent repository
	- sub module **can be updated** to the latest changes **without affecting the parent** repository and **vice versa**

###### FAQ
- How about clone/pull?
	- At once
		- `git pull` / `git clone` **pulls** **without** sub-modules. If you want to pull **with** sub-modules, add `--recursive-submodules <url>` with the url **optional**.
		  `git pull --recursive-submodules`
	- Separately
		- `git submodule init`: This command initializes the submodules by creating the corresponding directories in your local repository.
		- `git submodule update`: This command downloads the actual content of the submodules from their respective repositories and populates the initialized directories.
- Changes on the cloud sub module?
	- `git submodule update` or to check the updates `git submodule status`
# Why / When - I need it
- sharing library
- optional package
# Requirements
- The submodule repository must be **INITIALIZED** with a commit before being used
# How
## Setup
1. on your current repo root folder
```sh
tree -L 1
git submodule add $url $path
```
> your sub repo will be cloned & .gitmodules file will be generated
2. DONE
### Examples
```sh
# simple
git submodule add git@github.com:SugaryScripts/blackhole-sub-images.git
# full
git submodule add git@github.com:SugaryScripts/blackhole-sub-images.git Extra/Image
```
## Remove Sub Module
1. on root repo folder
>`$submodulename` => (example) = blackhole-sub-images
```sh
git config -f .git/config --remove-section submodule.$submodulename
git config -f .gitmodules --remove-section submodule.$submodulename
```
2. remove directory from index & commit changes of removal
```sh
git rm --cached $submodulepath
git add .gitmodules
git commit -m "Removed submodule $submodulename"
```
3. Delete unused files
```sh
rm -rf $submodulepath 
rm -rf .git/modules/$submodulename
```
4. DONE