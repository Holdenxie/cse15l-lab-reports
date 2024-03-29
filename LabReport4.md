# Lab Report 4
## log into ieng6
I used the `ssh` command to log into ieng6. In this case, `ieng6-202` is being connected. 
```
PS C:\Users\holde> ssh hax036@ieng6.ucsd.edu
Last login: Tue Feb 27 20:24:00 2024 from 128.54.173.18
quota: Cannot resolve mountpoint path /home/linux/ieng6/.snapshot/hourly.2024-02-19_2001: Stale file handle
quota: Cannot resolve mountpoint path /home/linux/ieng6/.snapshot/hourly.2024-02-19_1601: Stale file handle
quota: Cannot resolve mountpoint path /home/linux/ieng6/.snapshot/hourly.2024-02-20_0801: Stale file handle
quota: Cannot resolve mountpoint path /home/linux/ieng6/.snapshot/hourly.2024-02-20_1201: Stale file handle
quota: Cannot resolve mountpoint path /home/linux/ieng6/.snapshot/hourly.2024-02-21_0801: Stale file handle
quota: Cannot resolve mountpoint path /home/linux/ieng6/.snapshot/daily.2024-02-08_0010: Stale file handle
quota: Cannot resolve mountpoint path /home/linux/ieng6/.snapshot/daily.2024-02-13_0010: Stale file handle
quota: Cannot resolve mountpoint path /home/linux/ieng6/.snapshot/daily.2024-02-09_0010: Stale file handle
quota: Cannot resolve mountpoint path /home/linux/ieng6/.snapshot/daily.2024-02-10_0010: Stale file handle
quota: Cannot resolve mountpoint path /home/linux/ieng6/.snapshot/daily.2024-02-11_0010: Stale file handle
quota: Cannot resolve mountpoint path /home/linux/ieng6/.snapshot/daily.2024-02-12_0010: Stale file handle
quota: Cannot resolve mountpoint path /home/linux/ieng6/.snapshot/weekly.2024-01-21_0015: Stale file handle
quota: Cannot resolve mountpoint path /home/linux/ieng6/.snapshot/hourly.2024-02-20_1601: Stale file handle
quota: Cannot resolve mountpoint path /home/linux/ieng6/.snapshot/hourly.2024-02-20_2001: Stale file handle
quota: Cannot resolve mountpoint path /home/linux/ieng6/.snapshot/hourly.2024-02-19_1201: Stale file handle
quota: Cannot resolve mountpoint path /home/linux/ieng6/oce/7m/.snapshot/hourly.2024-02-24_1601: Stale file handle
Hello hax036, you are currently logged into ieng6-202.ucsd.edu

You are using 0% CPU on this system

Cluster Status 
Hostname     Time    #Users  Load  Averages  
ieng6-201   20:30:01   19  0.29,  0.65,  0.63
ieng6-202   20:30:01   23  0.22,  0.26,  0.22
ieng6-203   20:30:01   7   0.00,  0.10,  0.25 
```

## Clone the repository
I used the `git clone` command followed by my `ssh url` to clone the repository into my local computer.
When the repository of the fork is copied, the command `ctrl+shift+v` will allow you to paste it.
```
[hax036@ieng6-202]:~:118$ git clone git@github.com:Holdenxie/lab7.git
Cloning into 'lab7'...
remote: Enumerating objects: 58, done.
remote: Total 58 (delta 0), reused 0 (delta 0), pack-reused 58
Receiving objects: 100% (58/58), 376.39 KiB | 1.64 MiB/s, done.
Resolving deltas: 100% (21/21), done.
```

## Run the test 
Before running the test, I changed to `lab7` through the `cd` command. 
```
[hax036@ieng6-202]:~:120$ cd lab7
```
Then I compiled the java files using the command `javac` 
```
javac -cp .:lib/hamcrest-core-1.3.jar:lib/junit-4.13.2.jar *.java
```
Then I ran the code with the following. Since the class path is needed to be modified, I pressed `<up>` to get previous command 
and pressed `<right>` multiples times to get to the back of the line and pressed the `backspace` key to delete the existing class path and 
typed in the correct class path. 
```
java -cp .:lib/hamcrest-core-1.3.jar:lib/junit-4.13.2.jar org.junit.runner.JUnitCore ListExampleTests
```
## Editing the code 
I entered `vim` to edit the code by the following 
```
[hax036@ieng6-202]:lab7:125$ vim ListExamples.java
```
```
After I entered vim I entered `:set number` to show the line number of each line. Then I pressed the `<up>` and `<right>` key multiples times
until I reached line 44 and I used the `x` command to delte `1` and then use the `i` the command to insert `2`. Once I finished I used `:wq` to 
save and exit, then presed `<enter>` to quit vim. 
```

## Rerun the test 
I reran the test with the following the command and all the tests passed. 
```
[hax036@ieng6-202]:lab7:126$ javac -cp .:lib/hamcrest-core-1.3.jar:lib/junit-4.13.2.jar *.java
[hax036@ieng6-202]:lab7:127$ java -cp .:lib/hamcrest-core-1.3.jar:lib/junit-4.13.2.jar org.junit.runner.JUnitCore ListExamplesTests
JUnit version 4.13.2
..
Time: 0.014

OK (2 tests)
```

## Committing and Pushing 
the command `git command -a` is used to commit changes. This then opens a vim window forcing you to leave a commit message. 
```
Committer: Haolin Xie <hax036@ieng6-202.ucsd.edu>
Your name and email address were configured automatically based
on your username and hostname. Please check that they are accurate.
You can suppress this message by setting them explicitly. Run the
following command and follow the instructions in your editor to edit
your configuration file:

    git config --global --edit

After doing this, you may fix the identity used for this commit with:

    git commit --amend --reset-author

 1 file changed, 1 insertion(+), 1 deletion(-)
```

The changes can then be pushed through the `git push` command. 
```
[hax036@ieng6-202]:lab7:130$ git push
Enumerating objects: 5, done.
Counting objects: 100% (5/5), done.
Delta compression using up to 8 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 291 bytes | 145.00 KiB/s, done.
Total 3 (delta 2), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (2/2), completed with 2 local objects.
To github.com:Holdenxie/lab7.git
   327ab1a..e587936  main -> main
```
