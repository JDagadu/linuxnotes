# Linux
* linux generally is an operating system
* An operating system is a software that manages hardware resources to provide an environment for applications to run
* A linux distribution (distro or flavor) refers to a collection of software and specific applications bundled together and shipped as a single operating system
* The kernel is the core of the Os. It sits between the hardware and the software more like the intermediary between the hardware and the software.
* Apart from the kernel other components make  the OS useful like system libraries, web browsers, email utilities, user interfaces and other programs
* The two popular distros are redhat and ubuntu
* Others include Open SUSE, Fedora, Linux Mint, Debian, Mageia, Arch Linux, Slackware
## Linux Directory Structure Common directories
* / or root: is the top of the file system hierarchy
* /bin: binaries and other executable programs
* /etc: system configuration files
* /home: Home directories 
* /opt: optional or third party software
* /tmp: temporary space, typically cleared on reboot
* /usr: user related programs
* /var: variable data, most notably log files

## The shell
* The shell is the default user interface. 
* The graphical interface is also a shell a graphical shell
* also called the command interpreter

## The shell vs GUI
* the command line is more powerful
* there will always be a command line
* Server distributions have GUId and CLIs

* When the shell is started it displays a prompt
* the root user is the all powerful user
* the normal user can do a subset of things the root user can do
* Root access is typically restricted to admins
* Root access may be rwqured to install, start or stop an application.

## Basic Linux commands
linux is case has case sensitive commands
 #### Environmental variables
 * Storage location that has a name and a value
 * Typically uppercasing
* Path is an environment variable that controls the command search path
* Contains a list of directories

## files and directory permissions
* The three main types of permissions:
    * read
    * write
    * execute
* If you have read permissions to a file it means you have can view its contents eg cat filename
* If you have write you can change its contents 
* If you have execute you can run that file as a program

### Permissions - Files vs Directory
|Permission|File|Directory|
|----|-----|-----|
|Read|allows a file to be read|allows a file  names in the directory to be read|
|Write|allows a file to be modified|allows entries to be modified within the directory|
|execute|allows the execution of a file|allows the acess to contents and metadata for entries
### permission categories
* User (u)
* Group (g)
* Other (o)
* All (a)

* group: 
    * every user is in at least one group
    * Users can belong to many groups
    * groups are used to organize users
    * the *groups* command displays user's groups
    * You can also use *id -Gn*

### changing permissions(changing mode)
* command for changing mode is the *chmod* eg: chmod mode file
* the mode can be specified using symbolic notation or numeric notation
### working with groups
* New files belong to your primary groups
* the *chgrp* command changes the group

### File creation mask
* File creation mask determines default permissions
* If no mask were used permissions would be
    * 777 for directories
    * 666 for files
* masks are set by system admins
* to create a file without a mask by using the command *umask [-S] [mode]*

### Finding files and directory
* *find [path] [expression]* recursively finds files in path that match expression. If no arguments are supplied it find all files in the current directory
* locate  pattern is a faster find than find
    * lists files that natch pattern 
    *  faster than the find command 
    * queries an index 
    * results are not in real time
    * May not be enabled on all systems  
### Displaying the contents of files 
*  cat filename : displays contents of a file
* more file : browse through the file
* less file: more features than more command 
* head file: output the beginning portion of file 
* tail file : output the ending or bottom portion of file 
* by default head and tail displays 10 lines of file
* cat command is used for files that are static but the tail command can be used to follow a file that is constantly changing
* tail -f file will display data as it is being written to the file
### Editing files (nano editor)
* Nano is a simple editor. 
* Easy to learn.
* Not as advanced as vi or emacs.
* If nano isnt available, look for pico.
### vi editor
* Has advanced and powerful features 
* Not intuitive
* Harder to learn than nano
* Requires a time investment






