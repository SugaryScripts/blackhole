tag:: #git 


![](https://git-lfs.com/images/graphic.gif)
# What
Mostly git is used for tracking code as **text**. LFS is for saving a large file like jpg, mp4, that saved as **byte**.

# Why
Without LFS, each time you crop or change the jpg files, the git will make a **duplicate** as a snapshot for each commit. Makes it double storage consumption each commit a changes file.
# How
Instead of saved as byte, it only saved as address pointer or **reference** where the actual file are saved somewhere (LFS Server).

# Setup
```sh
pacman -S git-lfs
git lfs install
```

Declare what type of files that the lfs going to track
```sh
git lfs track "*.jpg" "*.png"
```
.gitattributes will be created


# Other Command
## Prune (remove local copies)
- **Purpose:** Removes the local copies of Git LFS objects (large files) from the working directory.
- **Effect:** Frees up storage on your local machine by deleting the actual content of Git LFS files, leaving behind only Git LFS pointers.
- **Usage:** `git lfs prune`

## Checkout (replace to pointer)
- **Purpose:** Replaces the actual content of Git LFS files in your working directory with Git LFS pointers.
- **Effect:** Minimizes the storage used by replacing the actual large files with lightweight pointers. It doesn't delete the files; it only replaces their content in the working directory.
- **Usage:** `git lfs checkout`

## **Verify** Git LFS Status:
Confirm that Git LFS is tracking the files or not
input:
```sh
git lfs ls-files
```
output:
```sh
eed9711b12 * Xinghai _ 星海.jpg
c64c871322 * Yin.full.53587.jpg
a1cef09712 * monika2.png
ca1705ce95 * tmblr not.png
9a6e56a24d * yuri.png
f9d5ec3adc * 嘘つき.png
74d17487cf * 鉄鋼の街.png
```

## **Verify Size** of the Repository


- Check the size of your Git repository after running the Git LFS commands. You can use the following command to see the size of the Git repository:
    
    bashCopy code
    
    ``
    
- Look for the `size-pack` value to see if it has decreased after running `git lfs prune`. This value represents the packed size of the Git objects.

