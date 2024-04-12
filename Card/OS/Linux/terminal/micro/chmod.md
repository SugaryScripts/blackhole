`chmod -R 755`

o change all the directories to 755 (`drwxr-xr-x`):

```
find /opt/lampp/htdocs -type d -exec chmod 755 {} \;
```

To change all the files to 644 (`-rw-r--r--`):

```
find /opt/lampp/htdocs -type f -exec chmod 644 {} \;
```
