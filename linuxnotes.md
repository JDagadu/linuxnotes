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
* *vi(m|ew)\* [filename]*
* vi has a concept of modes
    * command mode
    * insert mode
    * line mode
### Graphical editors
* emacs
* gedit
* gvim
* kedit
* AbiWord
* Kate 
* LibreOffice
### Wildcards
* a character or string used for pattern matching 
* globbing expands the wildcard pattern into list of fikes and/or directories
* wildcards can be used with most commands
    * ls 
    * rm 
    * cp
character class matches any of the characters included between the brackets. Matches exactly one character.
[aeiou]
ca[nt]*
[!aeiou]

### Input and Output
* standard input stdin   0
* standard output stdout 1
* standard error stderr  2

* \> redirects standard output to a file. Overwrites existing contents
* \>> redirects standard output to a file. appends to any existing contents
* Redirects input from a file to a command
### Comparing the contents of files
* diff file1 file2: compares two files
* sdiff file1 file2 side-by-side comparison
* vimdiff file1 file2 highlights differences in vim
### searching in files
* grep is used to search for a pattern in a file and display that pattern
* -i : perform a search, ignoring case
* -c: count the number of occurrences in a file
* -n: precede output with the line numbers
* -v: invert match. Print lines that don't match
 #### file command 
 displays file type
 #### strings 
 * displays printable strings in a binary file
 #### cut command 
 * cuts out selected portions of file. if file is ommitted use the standard input
 * -d delimiter uses delimiter as the field separator
 * -f N display the nth field
 #### copy files over the network
 * scp - secure copy 
 * sftp - ssh file transfer protocol
 * command line scp clients are 
    * scp
    * sftp
    * putty secure copy client
    * putty secure file transfer client
* graphical clients
    * cyberduck
    * filezilla
    * winscp
#### customizing the shell prompt
* use an environment variable to customize
* Bash, ksh and sh use $PS1
* to make your shell customizations persist between logins; echo 'export PS1="[\u@\h \w]\$" ' >> ~/.bash_profile
#### aliases 
* can be used to make shortcuts
 * use for long commands 
 * use for caommands you type often
 #### environment variables
* can change how an application behaves
* an example environment variable : EDITOR = nano
#### Processes and Jobs
* ps is used to display process status
#### Cron
* cron is a timebased job scheduling service
* crontab is a program to create, read, update, and delete your job schedules
use cron to schedule and automate tasks
    * \* minute
    * \* hour
    * \* day of the month
    * \* month of year
    * \* day of week
#### switching user 
* sudo is used to run commands as another user but its done as you being the root user

#### shell history
* Executed commands are added to the history
* Shell history can be displayed and recalled
* Shell history is stored in memory and on disk 
* HISTSIZE  is used to control the numbers of commands to retain in history

#### installing software on a debian distribution
* debian
* linux mint
* ubuntu
### The Linux Boot Process
* BIOS
* Basic Input/Output System
* Special firmware
* it's operating system independent
* Primary purpose is to find and execute the boot loader
* Performs the POST
    * Power on self test
* knowws about bootable devices 
    * Hard drives 
    * usb drives
    * dvd drives
* The boot device search order can be changed
* grub has replaced lilo as bootloader for linux
* bootloaders start the operating system
* boot loaders can start the operating system with different options
* initrd is the initial ram disk
* temporary filesystem that loaded from disk and stored in memory
* contains helpers and modules required to load the permanent OS file system
* boot directory contains the files required to boot linux
    * initrd
    * kernel
    * boot loader configuration
* kernel ring contains messages from the linux kernel
* dmesg
* /var/log/dmesg
* runlevels are used to determine the what processes and services to start
    * 0: shut down the system
    * 1,S,s: single user mode. used for maintenance 
    * 2: multi-user mide with graphical interface (debian/ubuntu)
    * 3: multi-user text mode (redhat/centos)
    * 4: undefined
    * 5: multi-user mide with the graphical interface.
    * 6: reboot
#### The syslog standard
* aids in the processing of messagees 
* allows logging to centrally controlled 
* uses facilities and severities to categorize messages
     * 0 : emerg
     * 1: alert
     * 2: crit
     * 3: err
     * 4: warn
     * 5: notice 
     * 6: info
     * 7: debug
* syslog servers : 
    * syslogd
    * rsyslog
    * syslog-ng
#### Disk Management
* Disks can be divided into parts called partitions
* Partitions allow you to separate data
* Partitioning schemes
    * os, applications, user, swap
    * os, user home directory
* can protect the overall system
* keep users from creating outages by using a home directory
* MBR is the master boot record
* can only address 2tb of disk space
* being phased out gpt
* 4 primary partitions
* extended partitions allow you to create logical partitions
* GPT is guid partition table
* guid is the global unique identifier
* replacing the mbr partioning scheme 
* part of the uefi 
* uefi is the unified extensible firmware interface 
* uefi is replacing bios
* supports up to 128 partitions
* supports up to 9.4 zb disk size
* not supported by older operating systems
* may require newer or special tools
* A mount point is a directory used to access the data on a partition
* / is always the a mount point
* fdisk is the partitioninng  tool that will be used for partitioning
* earlier versions of the fdisk not support gpt
* alternative verions of the fdisk are parted and gdisk
* before a partition can be used by the os it needs a file system
* the extended file system was created for linux
* often the default file system on linux
* in order to make mounts persist between reboots, add an entry in the /etc/fstab file
* etc/fstab contros what devices get mounted and where on boot
* each entry is made up of 6 fields
    * device
    * mount point
    * filel system type
    * mount options 
    * dump
    * fsck order
#### Logical Volume Manager (LVM)
* Why LVM?
* extra layers of abstraction between the storage devices and the file systems placed on those devices
* flexible capacity
* you can create fuke systems that extend across multiple storage devices
* you can aggregate multiple storage devices into a single logical volume
* expand or shrink file systems in real time while data remains oline fully accesible
* easily migrate data from one storage device to another while online
* you can use human readable device names with a descriptive name
* increase throughput by allowing to read data in parallel
* you can strike data across two devices
* increase fault tolerance and reliability by having more than one copy of your data
* create snapshots of your filesystems point in time snapshots
#### layers of abstraction
1. physical volumes: storage devices used for lvm. they dont have to be physical
1. volume group: made up of one or more physical volumes
1. Logical volume: created from a volume group. File systems are created on top them. as long as there is space on the volume group you can extend the logical volume
#### logical volume creation process 
* create one or more physical volumes
* create a volume group from those one or more physical volumes
* create one or more logical volumes from the volume group
### Managing users and groups
* Multiple accounts can exist and can be used at the same time
* All accounts have;
    * username (or login ID)
    * UID
    * default group
    * comments
    * shell
    * Home directory location
* all this information is stored in the /etc/password file
* *username:password:UID:GID:comments:home_dir:shell*
* linux supports username length up to 32 characters its customary to have usernames less than 8 characters
* case sensitive
* numbers are not allowed in username
* do not use  special characters
* in all lowercase by convention
* passwords are stored in the /etc/shadow file
* encrypted password used to be stored in /etc/passwd
* etc/passwd is readable by everyone
* now, encrypted passwords are stored in /etc/shadow
* etc/shadow is only readable by root
* prevents users trying to crack passwords
* when using the -m option the content of the /etc/skel are copied into the home directory
* etc/skel contains shell configurations
* group details are stored in the /etc/group file
* format for the file *group_name:password:GID:account1,accountN*

### Networking Linux
* TCP/IP
    * used for network communications
* tcp controls data exchange
* ip sends data from one device to another
* hosts are devices on a network that have an ip address
* for a device on a network to communicate successfully it needs:
    * ip address
    * subnet mask 
    * broadcast address
* each one of these are made up of 4 octets separated by a dot
##### IP networking
* IP addresses are comprised of two parts 
    * network address
    * host address
* each must be unique for proper routing
* address classes are used to determine the network address and host address.

|class |Network |Host allowed|
|------|------|-------|
|A|1.0 to 127.0|16,777,216|
|B|128.0 to 191.255|65,536|
|C|129.0 to 233.255.255|255|

#### subnet mask
|class |Network |
|------|------|
|A|255.0.0.0|
|B|255.255.0.0
|C|255.255.255.0

* host is a device connected to a network
* a hostname is simply a human readable name with an ipaddress assigned to it
* dns is used to translate human readable names into ip addresses the reverse is also true
* FQDN is a fully qualified domain name
* TLD is the top level domain
* domains are to the left of the tlds
* subdomain
* to resolve a dns name you can use the dig or host tool
* the /etc/hosts file contains a list of ip addresses and hostnames
* typically the dns server is checked first before the /etc/hosts file
* you can change this behaviour by editting the /etc/nsswitch.conf
* NSS stands for Name Service Switch
* controls the search order for resolutions
* Just like Ip addresses identify the hosts on a network, ports identifies the services on a host
* When a service starts it binds itself to a port and listens for traffic destined for its port
* Ports 1 - 1023 are well known ports (Privelege ports)
    * 22 - ssh
    * 25 - smtp
    * 80 - http
    * 143 - imap
    * 389 - ldap
    * 443 - https
* Ports above 1024 are unprivilege ports
* etc/services maps port names to port numbers
* here youll find a list of pre-defined ports and you can add to this list
* dhcp stands for dynamic host configuration protocol
* dhcp servers assign ip address to dhcp clients
    * ip address
    * netmask
    * gateway
    * dns servers
* each ip is leased from the pool of ip addresses the dhcp server manages
    * The lease expiration time is configur able on dhcp server. (1hr, 1day, 1week etc)
    * the client must renew the lease if it wants to keep using the ip adddress. if no renewal is reveived the ip is available to other dhcp clients
    * to configure an ubuntu client as dhcp edit the /etc/network/interfaces
* iface networkdevice inet dhcp
* you can also assign a static ip address to a client
* edit the etc/network/interfaces
* iface networkdevice inet static
    address ipaddress
    netmask 255.255.255.0
    gateway 10.109.155.1
* an easy way of bringing an interfacce up or down is by using the ifup/ifdown tool
* these are actually scripts 
* if you make a configuration change you can test it by using the ifup or ifdown commands
* instead of manually editting network configuration files some  distribution supply gui/tui tools
* gui stands for graphical user interface
* tui stands for textual user interface
* RedHat 
    * mmtui
    * system-config-network
* SUSE 
    * YaST
#### network diagnostics and troubleshooting 
* if youre having issues connecting to a host you should use the ping command
* traceroute is used to show the path before reaching a host
* netstat is used to get a variety of information about a network
    * -n displays the numerical addresses and ports
    * -i displays a list of network interfaces
    * -r displays the route table netstat(-rn)
    * -p displays the pid and program used
    * -l displays listening sockets (netstat -nlp)
    * -t limit the output to tcp (netstat -ntlp)
    * -u limit the output to udp (netsat -nulp)
* packet sniffing with tcpdump
* tcpdump
    * -n display numerical addresses and ports
    * -A displays ascii(text) output
    * -v verbose mode. Produce more output
    * -vvv even more verbose output
* The telnet command is obsolete, it was previously used to remotely connect to hosts but now ssh is used for that    
* Telnet can be used to troubleshoot network issues
#### Special Permission Modes
* when a process is started it runs using the starting user's uid and gid
* setuid = set user id upon execution 
* setuid files are an attack surfacee
* not honored on shell scripts
* setgid is very similar to setuid it causes the user to execute a file with the group priveleges of a file rather than the group priveleges of the user 
* set group id
* setgid on a directory carses new files to inherit the group of the directory 
* setgid causes directories to inherit the setgid bit
* it only affects the new files created after the setgid was added to the directory
* sticky bit use on a directory to only allow the owner of the file/directory to delete it

# Shell Scripting
* Contain a series of commands.
* An interpreter executes commands in the script.
* Anything you can type at the command line,
you can put in a script.
* Great for automating tasks
* Variable names can contain digits, letters, and underscore
* They can start with letters or underscore but cannot start with digit



