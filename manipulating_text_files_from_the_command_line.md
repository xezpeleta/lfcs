# Manipulating text files from the command line

redirection
```
$ command > file.txt
$ command >> file.txt (adding)
```
pipe
```
$ command | command
```

Different commands:
    * ls
    * cat
    * sed 
    * du
    * sort
    * head *
    * tail *
    * uniq *
    * grep
    * cut


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

Example II (du and sort)
```
$ du -sch /var/* | sort
0	/var/lock
0	/var/run
123M	/var/opt
138M	/var/lib
15M	/var/log
326M	total
4,0K	/var/backups
4,0K	/var/local
4,0K	/var/mail
4,0K	/var/tmp
51M	/var/cache
60K	/var/chef
888K	/var/spool
```

lets add the -h into the sort command.
```
$ du -sch /var/* | sort -h
0	/var/lock
0	/var/run
4,0K	/var/backups
4,0K	/var/local
4,0K	/var/mail
4,0K	/var/tmp
60K	/var/chef
888K	/var/spool
15M	/var/log
51M	/var/cache
123M	/var/opt
138M	/var/lib
326M	total
```

Example III (grep)
```
$ grep -rni backup /etc/passwd
14:backup:x:34:34:backup:/var/backups:/bin/sh
``` 

```
$ ls -l /etc | grep rc[0-9]
drwxr-xr-x 2 root root    4096 ene 19 14:12 rc0.d
drwxr-xr-x 2 root root    4096 ene 19 14:12 rc1.d
drwxr-xr-x 2 root root    4096 ene 19 14:12 rc2.d
drwxr-xr-x 2 root root    4096 ene 19 14:12 rc3.d
drwxr-xr-x 2 root root    4096 ene 19 14:12 rc4.d
drwxr-xr-x 2 root root    4096 ene 19 14:12 rc5.d
drwxr-xr-x 2 root root    4096 ene 19 14:12 rc6.d

```

Example IV (cat and cut)

If we filter the cat command output with cut we could decide to show the firs and seven columns of the file we are trying to see. (remember we could redirect into a new file as well with > newfile.txt)

```
$ cat /etc/passwd | cut -d: -f1,7
root:/bin/bash
daemon:/bin/sh
bin:/bin/sh
sys:/bin/sh
sync:/bin/sync
games:/bin/sh
man:/bin/sh
lp:/bin/sh
mail:/bin/sh
```







