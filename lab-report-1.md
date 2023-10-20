# Lab Report 1 - Remote Access and FileSystem (Week 1)
## `cd` command
No argument:
```
[user@sahara ~]$ cd
[user@sahara ~]$ 
```
The output is not an error. `cd` needs a path as an argument to move active directories. There are no arguments after `cd`, so there is no output. <br>
Path to directory as argument:
```
user@sahara ~]$ cd lecture1
[user@sahara ~/lecture1]$
```
The output is not an error. `cd` uses the relative path argument /lecture1 to move into the lecture1 directory. <br>
Path to file as argument:
```
[user@sahara ~/lecture1]$ cd README
bash: cd: README: Not a directory
```
The output is an error because the command was used in an incorrect way and an error message was printed. `cd` is meant to take a path to a directory as an argument, not to a file.

## `ls` command
No argument:
```
[user@sahara ~/lecture1]$ ls
Hello.class  Hello.java  messages  README
```
The output is not an error. Without an argument, `ls` prints a list of objects readily available in the currently active directory. <br>
Path to directory as argument:
```
[user@sahara ~/lecture1]$ ls messages
en-us.txt  es-mx.txt  ko.txt  zh-cn.txt
```
The output is not an error. Given a path, `ls` prints a list of objects readily available in the directory given by the path. <br>
Path to file as argument:
```
[user@sahara ~/lecture1]$ ls Hello.java
Hello.java
```
The output is not an error. Given a path to a file, `ls` prints a list of objects available in it; so just one.

## `cat` command
No argument:
```
[user@sahara ~/lecture1]$ cat
```
The output is not an error. When I pressed enter, the entire terminal froze and I had to create a new one. This is because given no argument, `cat` doesn't have anything to concatenate and keeps running. <br>
Path to directory as argument:
```
[user@sahara ~]$ cat lecture1
cat: lecture1: Is a directory
```
The output is an error. Given a path to a directory, there is nothing for `cat` to concatenate; no file for it to read. <br>
Path to file as argument:
```
[user@sahara ~]$ cd lecture1
[user@sahara ~/lecture1]$ cat README
To use this program:
```
The output is not an error. Given a path to file README, `cat` concatenated the contents of file README.
