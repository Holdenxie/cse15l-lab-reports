# Lab Report 3
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

# Clone the repository
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

# Run the test 
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
