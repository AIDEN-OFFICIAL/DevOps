## 🐧 Linux Basic Commands Cheatsheet

Linux is the foundational operating system for almost all servers and cloud environments in DevOps. Mastering its command-line interface is the first and most crucial step in your learning journey. This file contains a quick reference to the most common commands you'll use every single day.

### Essential Commands

| Command | Description | Example |
| :--- | :--- | :--- |
| `ls` | **L**i**s**ts files and directories in the current folder. | `ls -la` |
| `cd` | **C**hanges the current **d**irectory. | `cd Documents` |
| `pwd` | **P**rints the **w**orking **d**irectory (shows your current location). | `pwd` |
| `mkdir` | **M**a**k**es a new **dir**ectory. | `mkdir new_project` |
| `rm` | **R**e**m**oves a file or directory. | `rm old_file.txt` |
| `sudo` | **S**uper **u**ser **do**. Runs a command with administrator privileges. | `sudo apt update` |
|`ssh`|**S**ecure **s**hell cryptographic network protocol for securley accessig and managing computers over an unsecured network.|`ssh [username]@[hostname or ip_address`|
|`nano`|writing or editing a file|`nano filename.txt` ctrl x+y to save|
|`vim`|vim editor for file manipulations like editing|`i` for inserting, esc + `:q` for exit, e `:wq` for saving and quiting|
|`cat`|to view contents of a file|`cat filename.txt`|
|`shread`|to never let someone seee a file we can shread it|`shread filename.txt`|
|`cp`|to copy a file to another directory|`cp file.txt ./dir/dir2/file.txt`|
|`mv`| to move a file|`mv file.txt ./dir/dir2/file.txt`|
|`rm`|delete or remove a file|`rm file.txt`|
|`rmdir`|remove directory|`rmdir -r dir2`|
|`clear`|clear the terminal|`clear`|
|`whoami`|to find your username|`whoami`|
|`useradd`|to rename to another usrname|`sudo useradd newname`|
|`su`|switching user |`su another_username`|
|`exit`|exit from oe user to default user|`exit`|
|`sudo passwd `|setup password|`sudo passwd user_name`|
|`sudo apt install`|to install packages|`sudo apt install finger`|
|`man`|manuel for all commands |`man ls` `man cat` `man man` `man finger`|
|`whatis`|just like man with les info|`whatis finger`|
|`wget`|download any content from the internet|`wget https://bible.txt`|
|`curl`|to download contents from internet just like wget|`curl remote_link >  filename`|
|`zip`|to create zipfiles|`zip new_zip_name.txt old_name.txt`|
|`unzip`|to unzip a zip file|`unzip filename.zip`|
|`less`|just like `cat` command , but it lazyloads so 1 page at a time|`less file.txt`|
|`head`|to only see the begining of the file|`head filename.txt`|
|`tail`|to only see the end of the file contents|`tail filename.txt`|
|`cmp`|compare to files contents|`cmp file1.txt file2.txt`|
|`diff`|to see difference in to file contents if theye have some similarities|`diff file1.txt file2.txt`|
|`sort`|helps you sort the contents in a file |`cat filetxt (pipe symbol) sort `|
|`sudo find`|to find or search a file |`sudo find /dir -name 'bible'` `find . -type f -empty`|
|`chmod +x`|to execute a file|`chmod +x filename.txt`|
|`chown`|to change ownership of a file|`chown usernme`|
|`ifconfig`|to know the ip address and stuff |`ifconfig`|
|`ip address`|to know the ip address|`ip address`|
|`resolvectl status`|to see the DNS|``|
|`ping`|we can use to findout the status of a website , if it s hosted or not|`ping websitename.com``ping -c -5 websitename.com`|
|`netstat`|ports open on your linux|`netstat -tulpn`|
|`ufw`|allows or blocks ports |`sudo ufw allow 80`|
|`uname`|tells about the using system|`uname -a`|
|`echo`|if you want a result of some calculations|`echo'4+3+5+7' (pipe) bc`|
|`free`|to find free memory|``|
|`ps`|processes running|``|
|`htop`|prettier display of running processes|``|
|`kill`|to kill a process|find the process ID `kill -9 6656(PID)`|
|`history`|to find all recent commands that is used|``|
|`sudo reboot`|system reboot|``|
|`sudo shutdown`|shut down the system in 1 min|`sudo shutdown`|
|`alias`|to create shortcuts for longer commands|`alias mm='clear'` to see all aliases - `alias`|
|`grep`|'globally search a regular expression and print'find patterns in diff commands|`grep [options] pattern [file_name]`|
redirection > for storing the output of one command to a file , and >> for concatination of one file to another `echo "World" >> file.txt`
