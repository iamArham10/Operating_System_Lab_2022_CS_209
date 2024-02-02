---
typora-root-url: C:\Users\Win 10\Documents\GitHub\Operating_System_Lab_2022_CS_209\Lab3
---

#### UET Lahore Department of Computer Science

#### Operating System Lab

#### Arham Imran 	2022-CS-209

## Introduction to Ubuntu terminal commands

#### Echo (display text) : 

- 'echo' command is used to print anything on the terminal that you write after that command.![](/images/echo.png)
- 'echo -n' command is used to not move the prompt to the next line. ![](/images/echo-n.png)

#### Uptime (system uptime) :

- uptime command is used to show current time, number of users, system load averages, and for how long the system has been used. ![](/images/uptime.png)
  - '15:03:26' : Current Time
  - 'up 28 min' : The System has been up for 28 mins.
  - '2 users' : There are 2 users currently logged in.
  - 'load average : 0.62, 1.00, 1.05' : Load average(number of processes that are either in runnable or uninterruptible state) for last 1, 5, and 15 minutes, respectively.

#### PWD (Print-Working-Directory) :

- 'pwd' command is used to print working directory. It prints the current working directory, which is the directory you are currently in within the file system. ![](/images/pwd.png)
  - '/home/arham/Documents/OSLab' : Full path of the current directory you're in.

#### Mkdir (make directory) :

- 'mkdir' command is used to create directory. 
  ![](/images/mkdir1.png)
  - 'mkdir asia' : creates a directory of name 'asia' inside the current working directory.
- 'mkdir' command can also be used to create multiple directories. ![](/images/mkdir2.png)
  - 'mkdir Europe Africa America' : creates three directories Europe, Africa, and America inside the current working directory.
- 'mkdir -p' is used to create a directory inside a directory that also is not created. You can also use 'mkdir' only to create a directory inside a directory that is in the current directory. ![](/images/mkdir3.png)
  - 'mkdir -p Japan/Kobe' : creates a directory 'Japan' inside the current directory and 'Kobe' inside the directory 'Japan'.

#### Ls (List) :

- 'ls' command is used to list the files and directories in the current directory. ![](/images/ls.png)
- 'ls [directory path]' : You can also view directories and files inside the directory by giving the 'absolute' or 'relative' path of the directory after ls command. ![](/images/ls2.png)
- 'ls -a' lists all the files and directories including the hidden files.
- 'ls - l' command is used to list files and directories in long format. ![](/images/ls-l.png)
  - File Type and Permissions(e.g., 'drwxrwr-x') : indicates the type of file(directory, regular , etc.) and the permissions for the owner, group and others.
  - Number of Links : Displays the number of hard links to the file or directory.
  - Owner : Owner of the directory or file.
  - Group : Group associated with the directory or file. 
  - File Size : Size of the file.
  - Modification Time: Date and Time when the file or directory was last modified.
  - Name : Name of the file or directory.
- 'ls -lt' is used to show files in long format but files appears sorted by the modification time(t). The most recently modified files will appear at the top. If you want to include hidden files also you can add 'ls -lta'. ![](/images/ls-lt.png)
  - Most recently modified file is at the top, And so the trend continues.
- 'ls -ltr' is used to list files and directories in long format, sorted by modification time(t) in reverse order(r), with the newest files appearing at the bottom. ![](/images/ls-ltr.png)
  - Most recently modified file is at the bottom.

#### Whatis (short description of a specified command) :

- 'whatis' command is used to display a short description or one-line summary of a specified command. ![](/images/whatis.png)
  - 'whatsi date' displays the description of command date.

#### Man (Display documentation of a command) : 

- 'man' command is used to display the manual pages for a specified command. Manual pages provide information about command, utilities, and system calls. ![](/images/man.png)
  -  'man date' command shows the documentation of date command.

#### Help (Display information about built-in shell) :

- 'help' command is used in the shell to displey information about buil-in shell commands. It provides summary of the syntax and usage of shell commands. ![](/images/help.png)
  - 'date --help' command shows information about command 'date'.

#### Whoami(Display user name) :

- 'whoami' command is used to display the username of the current user. ![](/images/whoami.png)
  - 'whoami' : Displays current username 'arham'.



#### Cd (Current directory) :

- cd [directory path] : It will take you to the provided path directory. ![](/images/cd.png)
  - 'cd /home/arham/Documents' : Takes the current directory the Directory Documents.
  - 'cd OSLab' : Takes the current directory to the 'OSLab' directory that is inside Documents.

#### Touch (Create empty file or update the timestamp) :

-  'touch' command is used to create a new file or update the timestamps(access and modification times) of existing files. ![](/images/touch.png)
  - 'touch myfile.txt' creates a new file file with name myfile.txt. ![](/images/touch2.png)
- 'touch existingfile' will update the time stamp of the file name 'existingfile'.

#### Which (Locate executable file) : 

- 'which' command is used to locate the executable file associated with the given command. ![](/images/which.png)
  - 'which pwd' : prints the location of the executable file associated with command 'pwd'.

#### Cat, Head, Tail (Prints File Content) : 

- Cat command prints all the data inside the file on the terminal.
- Head command is used to display the beginning (head) portion of a file. Be default, it shows the first 10 lines of a file. You can specify number of lines using -n option.
- Tail command is used to display end(tail) portion of a file. By default, It shows the last 10 lines of a file. You can specify the number of lines by using '-n' option.
- ![](/images/catheadtail.png)
  - 'cat myfile' prints all the content in the file 'myfile.txt'.
  - 'head -1 myfile.txt' prints the first line of the file 'myfile.txt'.
  - 'tail -1 myfile.txt' prints the last line of the file 'myfile.txt'.
  - 'tail -2 myfile.txt' prints the last two lines.
  - 'head -2 myfile.txt' prints the first two lines of the file.

#### More (Display file content) : 

- 'more' command unlike 'cat' which displays all the content of the file. More command lets you navigate through the file interactively.
  - 'more new_file.txt' will open the file content and show on termina.
  - [Space] - scrolls the display, one screenful of data at a time.
  - [Enter] - scrolls the display by online.
  - [b] - scrolls the display backwards one screenful of data.
  - [/] - search for data.
  - Using More command.![](/images/more1.png)
  - After Pressing 'Enter'. ![](/images/more2.png)

#### Less (Improved Version of more) : 

- 'less' command is a improved version of more command. 
  - 'less filename' will open the file with name 'filename'.
  - [Up Arrow] - Scrolls up the display one line.
  - [Down Arrow] - Scrolls down the display one line.
  - [/] - search text.
  - After writing 'less filename' command.  ![](/images/less1.png)
  - Searching for word in 'rutrum' by writing /rutrum command. ![](/images/less2.png)

#### Nano (Text editor) : 

- 'nano filename' will open a terminal based text editor to edit file content.
- By writing 'nano myfile.txt' will open text editor allowing us to edit the file content. ![](/images/nano.png)

#### Id (Display information about user) :

- 'id' command is used to display information about user. ![](/images/id.png)
  - UID - User id.
  - GID - Group id.
  - Supplementary groups.
  - Other details.

#### Who (Display information of current user) : 

- 'who' command is used to display information about current user. ![](/images/who.png)
  - 'arham' user is logged in on the local terminal 'seat0'.
  - 'arham' user is logged in terminal 'tty2'.
  - 'arham' user is logged in pseudo-terminal 'pts/1' from different IP address.



 #### Last (Display recently login user details) :

- 'last' command is used to display recently logged-in users and their login sessions. It shows information about username, terminal, IP address, login time, and duration of the login session. ![](/images/last.png)

