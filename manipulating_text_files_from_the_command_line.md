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

'cat' command will show the content of the file gu.txt.

```
$ cat gu.txt
My name is Antton and my friend is Xabi.
I have a green tree.
You and I, we are friends.
```
We would manipulate 'gu.txt' with 'sed' and redirect the output into a new file 'gu2.txt', after that, check manipulated new file again with 'cat'. 
```
$ sed ‘s/y/Y/g’ gu.txt > gu2.txt
$ cat gu2.txt
MY name is Antton and mY friend is Xabi.
I have a green tree.
You and I, we are friends.
```
We would manipulate the previous created 'gu2.txt' file and change some text with characters. We would use the character ( ^ ) with 'sed' to represent the beginning of a line. (check the changes with 'cat') 
```
$ sed 's/and/\&/g;s/^I/You/g' gu2.txt
$ cat gu2.txt
MY name is Antton & mY friend is Xabi.
You have a green tree.
You & I, we are friends.
```






