# Editing text files on the command line

Most popular text editors: **Vi** and **Nano**

## Vi
The default editor that comes with the UNIX operating system is called *vi*.

Two modes:
* Command mode
* Insert mode

In the **command mode**, every character typed is a command that does something to the text file being edited.

In the **insert mode**, every character typed is added to the text in the file. Pressing `<Esc>` turns off the insert mode. 

### Start Vi

Edit file *readme.txt*:
```sh
$ vi readme.txt
```
Recover file *readme.txt* (that was being edited when system crashed):
```sh
$ vi -r readme.txt
```

### Exit from Vi

There are several ways to quit *vi*:
```
:x <Return> quit vi, writing out modified file to file named in original invocation
:wq <Return> -> quit vi, writing out modified file to file named in original invocation
:q <Return> -> quit (or exit) vi
:q! <Return> -> quit vi even though latest changes have not been saved for this vi call
```

### Commands
* Inserting text: **i**
* Inserting text (beginning current line): **I**
* Inserting text (ending current line): **A**
* Deleting single character: **x**
* Deleting entire current line: **dd**

More: http://www.cs.colostate.edu/helpdocs/vi.html

## Nano
