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
I have a green tree.
You and I, we are friends.

$ sed ‘s/y/Y/g’ gu.txt > gu2.txt
$ cat gu2.txt
MY name is Antton and mY friend is Xabi.
I have a green tree.
You and I, we are friends.

$ sed 's/and/\&/g;s/^I/You/g' gu2.txt
$ cat gu2.txt
MY name is Antton & mY friend is Xabi.
You have a green tree.
You & I, we are friends.
```

The ^ act only on the beginning of the line.





