## 🐧 Linux Basic Commands Cheatsheet


Linux is the foundational operating system for almost all servers and cloud environments in DevOps. Mastering its command-line interface is the first and most crucial step in  your learning journey. This file contains a quick reference to the most common commands you'll use every single day.
- open source OS
- built on Unix OS
- very secure
- can have access to the entire system

## Linux Architecture Components
Kernel, System Libraries, User Space, Shell, System Utilities, Daemons, and Configuration files.
- Kernel: Central part of Linux OS. Provide Interface between the user and computer harware
- System libraries: System libraries are **collections of pre-written code** that provides common functions for other programs to use.
- User Space: refers to the programs and apps that run on top of the OS
- Shell: CLI that allows user to interact with the Linux OS
- Daemons: background processes that run continuously and perform specific tasks such as network services, log management, etc.
- Configuration files: used to configure Linux Os system such as the Network settings, system settings, security settings etc.

## Linux Distros (Distributions)
Different verisions of Linux OS ex: Ubuntu, Fedora, Debian, CentOS, Mint, Red Hat Enterprise Linux (RHEL), etc.

## Linux files system 
the way in which the operating system organizes and stores files and directories on a computer's hard drive or other storage devices.
* hierarchial structure
### Types of File system:
- Ext4: widley used, high performance, reliability, and scalability.logs every changes
- XFS: optimized for large-scale data storage and is commonly used in enterprise and high-performance computing environments
- Btrfs: new, designed to be flexible, scalable, and easy to manage. Easy backup and restore data
- NTFS: a file system commonly used in Microsoft Windows
- FAT32: used in older Microsoft Windows systems. lots of limitations.

## Organization of Linux File System
```
/bin - contains essential command-line utilities that are required for the system to function
/boot - contains files needed for booting the system including the Linux kernel and boot loader configuration files
/dev - contains device files that represent various devices and hardware components on the system
/etc - contains configuration files for the system and various applications
/home - contains the home directories for individual users
/lib - contains libraries needed by the utilities in /bin and /sbin
/media - a mount point for removable media such as CDs, DVDs, and USB drives
/mnt - a mount point for temporarily mounting file systems
/opt - contains third-party software packages
/proc - A virtual file system that contains information about the system's process and kernel
/root - the home directory for the root user
/sbin - contains system executables, similar to /bin
/sys - A virtual file system that provides an interface to the kernel's device drivers
/tmp - Contains temporary files that can be deleted by the system when space is needed
/usr - contains user utilities and libraries as well as data shared by multiple users
/var - contains variable data such as log files, mail spools, and database files
```
### Essential Commands

| Command | Description | Example |
| :--- | :--- | :--- |
| `ls` | **L**i**s**ts files and directories in the current folder. | `ls -la`|
| `cd` | **C**hanges the current **d**irectory. | `cd Documents` |
| `pwd` | **P**rints the **w**orking **d**irectory (shows your current location). | `pwd` |
| `mkdir` | **M**a**k**es a new **dir**ectory. | `mkdir new_project` |
| `rm` | **R**e**m**oves a file or directory. | `rm old_file.txt` |
| `sudo` | **S**uper **u**ser **do**. Runs a command with administrator privileges. | `sudo apt update` `sudo -s` super user mode|
|`ssh`|**S**ecure **s**hell cryptographic network protocol for securley accessig and managing computers over an unsecured network.|`ssh [username]@[hostname or ip_address`|
|`nano`|writing or editing a file|`nano filename.txt` ctrl x+y to save|
|`vim`|vim editor for file manipulations like editing|`i` for inserting, esc + `:q` for exit, e `:wq` for saving and quiting|
|`cat`|to view contents of a file, and concatenate is also another use|`cat filename.txt`|
|`shread`|to never let someone seee a file we can shread it|`shread filename.txt`|
|`cp`|to copy a file to another directory|`cp file.txt ./dir/dir2/file.txt`|
|`mv`| to move a file|`mv file.txt ./dir/dir2/file.txt`|
|`rm`|delete or remove a file|`rm file.txt`|
|`rmdir`|remove directory|`rmdir -r dir2`|
|`clear`|clear the terminal|`clear`|
|`whoami`|to find your username|`whoami`|
|`useradd`|to rename to another usrname|`sudo useradd newname`|
|`userdel`|to delete a user|`sudo userdel newname`dont delete home directory.`-r` for dleteing home dir also|
|`su`|switching user |`su another_username`|
|`exit`|exit from oe user to default user|`exit`|
|`wc`|gives the count of the content in a file like the lines, words and characters|`wc flename` `wc filename -L` length of the longest line|
|`sudo passwd `|setup password|`sudo passwd user_name`|
|`sudo apt install`|to install packages|`sudo apt install finger`|
|`man`|manuel for all commands |`man ls` `man cat` `man man` `man finger`|
|`whatis`|just like man with les info|`whatis finger`|
|`wget`|download any content from the internet|`wget https://bible.txt`|
|`curl`|to download contents from internet just like wget|`curl remote_link >  filename`|
|`zip`|to create zipfiles|`zip new_zip_name.txt old_name.txt`|
|`unzip`|to unzip a zip file|`unzip filename.zip`|
|`less`|just like `cat` command , but it lazyloads so 1 page at a time|`less file.txt`|
|`head`|to only see the begining of the file|`head filename.txt` `head -n3 filename` to add numbers of line|
|`tail`|to only see the end of the file contents|`tail filename.txt`|
|`cmp`|compare to files contents|`cmp file1.txt file2.txt`|
|`diff`|to see difference in to file contents if theye have some similarities|`diff file1.txt file2.txt`|
|`sort`|helps you sort the contents in a file |`cat filetxt (pipe symbol) sort `|
|`sudo find`|to find or search a file |`sudo find /dir -name 'bible'` `find . -type f -empty` `find /dir -mtime +2` search files that is created before 2 days|
|`chmod +x`|to execute a file|`chmod +x filename.txt` give read , write and execute permissions , rwx|
|`chmod u+rw filename`|give permissionn to the user `u`, or group `g` or others `o` to read `r` , write `w` and execute `x`|`chmod u-w dir`cannot write on some directory for users|
|`chown`|to change ownership of a file|`chown usernme`|
|`ifconfig`|to know the ip address and stuff |`ifconfig`|
|`ip address`|to know the ip address|`ip address`|
|`resolvectl status`|to see the DNS|``|
|`ping`|we can use to findout the status of a website , if it s hosted or not|`ping websitename.com``ping -c -5 websitename.com`|
|`netstat`|ports open on your linux|`netstat -tulpn` `-p`for PID's `-l` listening ports |
|`ufw`|allows or blocks ports |`sudo ufw allow 80`|
|`uname`|tells about the using system|`uname -a`|
|`echo`|if you want a result of some calculations|`echo'4+3+5+7' (pipe) bc`|
|`free`|to find free memory|``|
|`ps`|processes running|`ps -ux`for list of running processes. `ps -aux`|
|`htop`|prettier display of running processes|``|
|`kill`|to kill a process|find the process ID `kill -9 6656(PID)`or `kill -KILL PID`|
|`history`|to find all recent commands that is used|``|
|`sudo reboot`|system reboot|``|
|`sudo shutdown`|shut down the system in 1 min|`sudo shutdown`|
|`alias`|to create shortcuts for longer commands|`alias mm='clear'` to see all aliases - `alias`|
|`grep`|'globally search a regular expression and print'find patterns in diff commands|`grep [options] pattern [file_name]` options:-i = caseInsensitivity ,-n=line number |
|`top`|provides a real-time, dynamic view of a running system.|`top` press **i** for idle processes , press **k** and kill with PID|
|`pidof`|to find the process id of a certain process|if you know the name of a process `pidof name`|
|`which`|fid the location of files,commands etc..|`which bash` to find the location of the bash, `which cat`|
|`whatis`|what a command is for , or a shortest description of a command|`whatis grep` `whatis ls`|
|`groups`|to list all the groups a user is part of|`groups`, all groups in system - `cat/etc/groups`|
|`sudo groupadd name`|to add new groups|`sudo groupadd cpp`|
|`sudo groupdel name`|to delete a groups|`sudo groupdel cpp`|
|`sudo gpasswd -a usrname grpname`|add one user to another grp||
|`du`|to check the memory usage of a file or dir|`du -sh` show disk usage in human readable format|
|`df`|to check the memory usage and free mem of a file or dir|`df -h`|
|`cal`|calander|`cal year` `cal mnth yr`|
|`date`|date command to change the date of the system|`date -s "11/02/2026 12:00:40"` `cal mnth yr`|
|`;` `&&`|we combine any two commands and get a combined result in a single go|`cal ; date ; pwd` `cal&&pwd&&cal`|
|`ifconfig`|whole configurations of the network connections |`ifcconfig` `ifconfig eth0 down` the eth0 will be disconnected `ifconfig eth0 up`|
### Notes
to execute a file you can use `./fiename` on the shell
redirection > for storing the output of one command to a file , and >> for concatination of one file to another `echo "World" >> file.txt`

### How to setup Opesn ssh
`ssh` to check weather ssh clien is installed

`ssh user@ip -P122` to check ssh client is setup (ssh username and IP with port) example `ssh user@192.168.1.10`
Once connected, you can run Linux commands on that remote machine.


`ssh localhost` check ssh server is installed

install ssh server: `ssh apt-get install openssh-server` then give password

File transfer:
Local → Remote
`scp file.txt username@server_ip:/home/username/` (scp-secure copy)

Remote → Local
`scp username@server_ip:/path/to/remote/file.txt /path/to/local/destination/`


SSH can create secure tunnels for other applications.

Automation & DevOps:
In system administration, SSH is used by scripts and tools (like Ansible or Git) to manage servers without typing passwords every time (using SSH keys).
Services like AWS EC2, DigitalOcean, or Google Cloud let you connect to your virtual servers (droplets or instances) using SSH.


SSH Keys (instead of passwords):
SSH can use key-based authentication, which is more secure than typing a password each time.
You create a public/private key pair:
`ssh-keygen`
Then copy your public key to the server:
`ssh-copy-id username@server_ip`
After that, you can log in without a password.

### shortcuts
`ctrl+shift` for a new tab of terminal

# References:
https://devops.pradumnasaraf.dev/linux/commands
