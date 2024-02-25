
![](https://git-lfs.com/images/graphic.gif)
# What
Mostly git is used for tracking code as **text**. LFS is for saving a large file like jpg, mp4, that saved as **byte**.

# Why
Without LFS, each time you crop or change the jpg files, the git will make a **duplicate** as a snapshot for each commit. Makes it double storage consumption each commit a changes file.
# How
Instead of saved as byte, it only saved as address pointer or **reference** where the actual file are saved somewhere (LFS Server).

# Setup



