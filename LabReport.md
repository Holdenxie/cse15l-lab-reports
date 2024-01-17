# **Haolin Xie's Lab Report**

## `cd` command with no argument
```
[user@sahara ~]$ cd
[user@sahara ~]$ pwd
/home
```

The working directory is `home` when the command is ran with no arguments.
When no argument is given to the cd command, the current directory will be changed to the user's home directory. 
In this case, the working directory is already the user's home directory, therefore, there is no changes to the directory. 
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

The working directory is `home/lecture1/messages` when the command is ran with `ar-dz.txt` as an argument. 
This is because `ar-dz.txt` is not a valid argument for this command, thus the working directory does not change. 
The output is an error message because I ran the command with an invalid argument, as the output states that the file, `ar-dz.txt` is not a directory.

## `ls` command with no argument

```
[user@sahara ~]$ ls
lecture1
```
The working direcotry was `home` when the command is ran. 
When the `ls` command is ran with no argument, it will list all the files and directories in the current directory.
Since `lecture1` is the only directory in the current directory, it is the only one that is listed.
The output is not an error because it represents all the direcotires and files within the `home` directory.

## `ls` command with a `directory` as an argument 

```
[user@sahara ~]$ ls lecture1
Hello.class  Hello.java  messages  README
```

The working direcotry was `home` when the command is ran. 
When the `ls` command is ran with `lecture1` as the argument, it will list all the files within `lecture1`. 
Since there are multiple files within `lecture1`, all those is listed. 
The output is not an error because only and all the files within `lecture1` are listed.

## `ls` command with a `file` as an argument 

```
[user@sahara ~/lecture1/messages]$ ls ar-dz.txt
ar-dz.txt
```

The working directory was `home/lectur1/messages` when the command is ran. 
when the `ls` command is ran with the file `ar-dz.txt`, itself is listed.
This is because the file `ar.dz.txt` only contains itself, thus it can only list itself. 
This is not an error message because the expected output and the output are identical. 

## `cat` command with no argument 

```
[user@sahara ~]$ cat

```

The working directory was `home` when the command is ran. 
When the `cat` command is ran with no argument, where there is input, no output is given because the commands reads the file and gives it an output. 
This is not an error because no argument was given, so there would not be any output. 

## `cat` command with a `directory` as an argument 

```
[user@sahara ~]$ cat lecture1
cat: lecture1: Is a directory
```
The working directory was `home` when the command is ran. 
When the cat command is ran with `lecture1` as the argument, an error message is outputted because the `cat` command cannot reads what's in a directory.
This is an error message because it takes in files as arguments rather than directories. 

## `cat` command with a `file` as an argument 

```
[user@sahara ~]$ cat lecture1/messages/zh-cn.txt
你好世界
```
The working directory was `home`.
When the `cat` command is ran with `home/lecture1/messages/zh-cn.txt` as an argument, the output would be what's inside the `zh-cn.txt` file.
This is not an error because `你好世界` is inside the `zh-cn.txt` file, which is identitical to the output. 
