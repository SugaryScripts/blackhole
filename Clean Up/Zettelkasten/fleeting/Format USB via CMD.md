```sh
diskpart
list disk
select disk 3
clean
create partition primary
format fs=ntfs quick
```
