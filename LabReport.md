# **Haolin Xie's Lab Report**

## `cd` command with no argument
```
[user@sahara ~]$ cd
[user@sahara ~]$ pwd
/home
```

The working directory is `home` when the command is ran with no arguments.
Though the command changes dirctory, but there isn't any input so the directory remains unchanged. 
The output is not an error because it started and ended in the same directory. 

## `cd` comamnd with a `directory` as an argument 

```
[user@sahara ~]$ cd lecture1
[user@sahara ~/lecture1]$ pwd
/home/lecture1
```

The working directory changed from `home` to `home/lecture1` when the command is ran with the `lecture1` as the argument.
This is the output because the `cd` comamnd changes directories and with the argument of `lecture1` the directory is changed to `home/lecture1`.
This output is not an error because it correclty changed from the original directory to the directory that's inputed as an argument. 

## `cd` command with a `file` as an argument 

```
[user@sahara ~/lecture1/messages]$ cd ar-dz.txt
bash: cd: ar-dz.txt: Not a directory
```

The working directory remain unchanged when the command is ran with a `ar-dz.txt` as an argument. 
This is because `ar-dz.txt` is not a valid argument for this command, thus the working directory does not change. 
This is not an error because I ran the command with an invalid argument, as the output states that the file is not directory, so the directory will remain unchanged. 

## `ls` command with no argument

```
[user@sahara ~]$ ls
lecture1
```


