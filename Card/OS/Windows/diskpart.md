launch as administrator
```sh
diskpart
list disk
select disk x
clean
create partition primary size=1024 | 4096
format fs=fat32 quick
assign
create partition primary
format fs=ntfs quick
assign
exit
```

fix disk
```
chkdsk D: /f /r /x
```