> Its Nested Repository

up:: [[Git]]
tags:: #vc/git

# What
- It's **like a package manager** but it's git. 
- **Independent** entities within a parent repository
	- **changes** are saved **different** from the parent
		- Each changes on sub must be **committed within that sub** only
		- Changes on parent must be **committed on root folder** parent repository
	- sub module **can be updated** to the latest changes **without affecting the parent** repository and **vice versa**

## FAQ
- How about clone/pull?
	- At once
		- `git pull` / `git clone` **pulls** **without** sub-modules. If you want to pull **with** sub-modules, add `--recursive-submodules <url>` with the url **optional**.
		  `git pull --recursive-submodules`
	- Separately
		- `git submodule init`: This command initializes the submodules by creating the corresponding directories in your local repository.
		- `git submodule update`: This command downloads the actual content of the submodules from their respective repositories and populates the initialized directories.
- Changes on the cloud sub module?
	- `git submodule update` or to check the updates `git submodule status`
- Changes on sub module local? [[#Save Changes on Sub Module]]
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
> your sub repo will be cloned & `.gitmodules` file will be generated
2. DONE
### Examples
```sh
# simple
git submodule add git@github.com:SugaryScripts/blackhole-sub-images.git
# full
git submodule add git@github.com:SugaryScripts/blackhole-sub-images.git Extra/Image
```
> Extra/Image are not created yet
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

## Save Changes on Sub Module
Just like a regular repository
1. Go to your sub module directory `cd $sub-module-directory`
```sh
git commit -am "Changes on sub module"
```
2. Make sure you have the correct remote on your sub module `git remote -v` then push
```sh
git push $remote $branch_name
```
3. (**Optional** on other machine) Update with newest changes from the cloud with `git submodule update`

# Troubleshoot
## Detached head

source:: [Why is my Git Submodule HEAD detached from master? - Stack Overflow](https://stackoverflow.com/questions/18770545/why-is-my-git-submodule-head-detached-from-master)

```sh
cd submodule
git checkout main
```
### Solution 1: Use options in command line

```bash
# cd back to project root
git submodule update --remote --merge
# or
git submodule update --remote --rebase
```

Recommended alias:

```bash
git config alias.supdate 'submodule update --remote --merge'

# do submodule update with
git supdate
```
### Solution 2: Add options into config file

Another solution is to change submodule update behavior in the `gitmodule` file by by setting `submodule.$name.update` to `merge` or `rebase`. It basically means you can do `git submodule update --remote` without passing `--merge` or `--rebase` explcitly, but read from config file automatically.

Here's an example about how to config the default update behavior of submodule update in `.gitmodule`.

```
[submodule "bash/plugins/dircolors-solarized"]
    path = bash/plugins/dircolors-solarized
    url = https://github.com/seebi/dircolors-solarized.git
    update = merge # <-- this is what you need to add
```

Or configure it through command line,

```bash
# replace $name with a real submodule name
git config -f .gitmodules submodule.$name.update merge
```

# Command
> $..- means optional with '-' at the end
```sh
"clone with specific sub module if there are many"
git clone --recurse-submodules $url-

"add sub module within a repo"
git submodule add $url- $path-

"equivalent with pull"
git submodule update

git submodule status
```






