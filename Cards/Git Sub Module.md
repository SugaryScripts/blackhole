> Its Nested Repository

up:: 
tags:: #git

# What
Separate repository that exist within a repository. It's like a package manager but it's git. 
###### FAQ
- Commit changes?
	- 
# Why / When - I need it
- sharing library
- optional package
# How
## Setup
1. on your current repo root folder
```sh
tree -L 1
git submodule add $url $path
```
> your sub repo will be cloned & .gitmodules file will be generated
2. DONE
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