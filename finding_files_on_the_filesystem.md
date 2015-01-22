# Finding files on the filesystem

find [directory_to_search] [expression]

Advanced find:
```
$ find . -maxdepth 3 -type f -size +2M
$ find /home/user -perm 777 -exec rm '{}' +
$ find /etc -iname "*.conf" -mtime -180 -print
```