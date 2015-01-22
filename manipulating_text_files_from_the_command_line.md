# Manipulating text files from the command line

redirection
```
$ command > file.txt
$ command >> file.txt (adding)
```

* different commands:
    cat 
    tail 
    head 
    sed

example I (cat and sed)

```
$ cat gu.txt
My name is Antton and my friend is Xabi.

$ sed ‘s/y/Y/g’ gu.txt > gu2.txt
$ cat gu2.txt
MY name is Antton and mY friend is Xabi. 
```
