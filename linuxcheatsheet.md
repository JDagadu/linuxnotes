* ls [directoryname]: displays directory contents, it can also give details about directories and files
 * cd [directoryname]: changes current directory
 * pwd : displays the present working directory
 * cat [filename]: concatenates and displays files
 * more [filename]: browse through a text file
* less [filename]: browse through a file with more options
* head [filename]: display the beginning by default 10 lines of the file
* tail [filename]: display the end by default 10 lines of the file
 * echo [arguments]: displays arguments too the screen
 * man [command]: displays the online manual
 * exit: exits the shell or your current session
 * clear: clears the screen
* echo $VAR_NAME: access contents of environmental variables
* chmod [g|u|o][+|-][r|w|x] [filename] = change user, group,other permissions for a file or directory
* chown user:group filename: to change the owner of a file 
chgrp [groupname][filename]: change the group the file or folder belongs
* find [directory] [-name|iname|-type|-size|-time|-newer] pattern: used to search for files or folders that match a specific pattern
* locate [pattern]: searches the index for files and folders that matches the pattern

### Vi editor commands
* vi [filename]: enters the vi edit mode
* hjkl: are used to move up left right character by character
* bw: are used to move left and right word by word
* ^$: go to the beginning and end of a line
* iI: to insert at the current cursor position or at the beginning of the line
* aA: to insert text after the cursor position or at the end of the line
* x : delete a character
* dw: delete a word
* dd: delete a line
* D: delete from current position to the end of the line
* r: replace a current character
* cw: change the current word
* cc: change the current line
* c$,C: change the text from the current position
* ~: reverses the case of a character
* yy: to yank(copy) a current line
* y \<position>: yank the position
* p: will paste the most recently yanked text
* u: undo
* ctrl-r: redo

#### Line mode
*:w,:w!: writes or saves a file or forces file to be saved
* :q,:q!: quit or force quit
* :wq,x: write and quit
* :n : positions cursor at line n
* :$ : positions cursor on the last line
* :set nu : shows the line numbers
* :set nonu: removes the line numbers
* :help [subcommand] gets help
* /\<pattern>: starts a forward search 
* ?\<pattern>: starts a reverse search

###
* rm [file] : remove file
* rm -r dir: remove the directory and its content recursively
* rm -f file: force removal and never prompt for confirmation
* ls s* : display any file or directory that matches this pattern
* rm s* : remove any file that matches the pattern
* cp sourcefile destinationfile: copy the sourcefile to the destination file
* cp sourcefile1[...sourcefileN] destinationdir: copies the list of files to the destinantion dir
* cp -i: run in interactive mode
* cp -r source directory destination_dir: copies source directory into destination directory, if the destination directory doesn't exist it creates it
* mv [-i] source destination: moves file from the source to the destination 
* sort file: sorts text as appears in the file alphabetically 
* sort -r: sorts in reverse order
* sort -u: removes duplicates
* sort -kF: sort by key. F is the field number
* tar [-] c|x|t f tarfile [pattern]: create extract or list contents of a tar archive using pattern, if supplied
* tar cf arch.tar directory: creates the archive
* gzip: compress file
* gunzip: uncompress files 
* gzcat: concatenate compressed files
* zcat: concatenates compressed file
* du : estimates file usage
* du -k :display sizes in kilobytes
* du -h: displays sizes in human readable format
* grep [option] pattern file: displays the line that matches the pattern
* file filename: displays the type of file
* strings filename: displays binary file in readable format
* scp source destination : copy source to destination 
* sftp host: start a secure file transfer session with host
* ssh host: used to start a session with the host server
* PS1="style": customizes shell to the new style
* alias:lists all aliases currently saved
* alias nameofalias='what alias should actually do'
* unalias name: remove alias  with that name
* unalias -a: remove all aliases
* printenv : displays all the environment variables set
* echo $VARIABLE: same as above
* export VAR="value": sets the environment variable to the value
* unset VAR: removes the value for the environment variable
* ps: diplays process status
* ps -e : displays everything all process
* ps -f: displays in a full format listing
* ps -u username: display username's processes
* ps -p pid: displays information for PID
* ps -e --forest: displays a process tree
* ps -eH: display a process tree
* pstree: display processes in a tree format
* top: interactive process viewer
* htop: interactive process viewer
* command &: starts command in background
* ctrl-c: kills command in the foreground
* ctrl-z: suspends the foreground process
* bg [%num]: background a suspended process
* fg [%num] foreground a background process
* kill [-signal] [%num]
* jobs [%num]: list jobs

#### cron
* crontab file: installs a new crontab from file
* crontab -l: list your  cron jobs
* crontab -e: edit your cron jobs
* crontab -r: remove all of your cron jobs
* 0 7 * * 1 some binary file: runs the job every monday at 7 
* su [username] : changes user ID or become superuser
* su - : creates an environment as that user 
* su -c : specify a command 
* whoami: displays which current user you are 
* sudo -l: list available commands to run with sudo
* sudo command : run command as root account
* sudo -u root command: same as above
* sudo -u user comand: run as user
* sudo su : switch to the superuser account
* sudo su - : switch to the superuser account with root's environment
* sudo su - username: switches to the username account with username environment
* sudo -s : start shell
* sudo -u root -s : starts a shell as root
* history : displays the shell history
* !N : repeat command on line command N
* !! | ! : repeat the previous command line
* !string: repeats the most recent command that matches the string pattern
* !:N : picks the nth arguments of the previous command
* !^: picks the first argument of the previous command
* !$: picks the firdt argument of the previous command
* apt-cache search string: searches for the string to see if that package is available
* apt-get install [-y] package: installs package, if the option y is included it answers yes for any type of questions asked during the installation 
* apt-get remove package: remove package, leaving configuration
* apt-get purge package: remove package with all its configuration
* apt-cache show package: shows information about package
* dpkg -l : list installed packages
* dpkg -S /path/to/file: list files package
* dpkg -L package: list all the files in package
* dpkg -i package.deb: installs package
* systemctl set-default graphical.target: sets the mode to boot with to graphical ui
* systemctl isolate graphical.target: changes the mode to graphical ui
* mail.* [-] /path/to/log/file: sends all mail messages to that log file when there is a hyphen it means its cached and isnt synchronized
* logger  [-p] mail.info -t [tag] message: used to test the directive above
* logrotate -fv /etc/logrotate.conf: used to force a test of editted logrotate file
* fdisk /path/to/device: used to begin partition utility and follow the prompts
* fdisk -l : displays a list of devices and their partition information
* mkfs -t type device: is used to make create a filesystem
* mkfs -t ext3 dev/sdb
* ls -l  /sbin/mkfs*: lists all the various types of mkfs
* mount dev/sdb3 /opt: used to mount a device on the directory
* mount : displays the what is currently mounted
* dh -h: displays a short list of the currently mounted file systems and their disk usage
* umount directory  or device/path: used to unmount partition
* mkswap path/to/partition: prepares the swap for use
* swapon path/to/device : to enable the swap partition
* swapon -s : shows all the swap devices in use
* lsblk -f: used to view labels and uuids of the device partitons
* blkid : only for uuids
* e2label path/to/dev label: it edits the labels for ext file system in the partition
### LVM 
* lvmdiskscan : checks all the available disks you can use for the task
* lsblk -p: used to get more information to see which device the root file has been mounted on shows mountpoint
* df -h: displays sizes in a human readable format
* pvcreate device: used to initializes the disk for use
* pvs: displays all the pvs 
* vgcreate nameofvolumegroup : creates the volumegroup
* vgs: displays the volume groups
* lvcreate -L size -n nameoflogicalvolume nameofvolumegroup: creates the logical volume with size and on the volumegroup provided
* lvdisplay : displays the logical volume in a different forrmat
* lvcreate -l sizeinextent or asapercentage -n nameoflv vg: creates a logical volume by squeezing the the very last extent available
* vgextend volumegroup physicalvolume: extends the volume group to the added physical volume
* lvextend -L +5G -r path/to/logicalvolume: extends the size by adding the size specified in the command
* lvcreate -m 1: creates 1 copy a mirror of data
* lvremove pathtologicaldevice: removes the logical volume with all its data after the filesystem has been unmounted
* vgreduce volumegroup physicalvolume: reduces the extent of the volumegroup making the physical volume accessible by some other vg
* pvremove device: reverts the device back to default and is no longer a physical volume
#### Account Management
* useradd [options] username: creates an account
    * -c : comments for the account
    * -m : create the home directory
    * -s : shell path
    * -g : specify default groups
    * -G group1,groupn : additional groups
    * -d : provides a path for the home directory
    * -r : creates a system account
    * -u : provides a uid
        * useradd -c "Eddie Harris" -m -s /bin/bash -g sales -G projectx eharris
* passwd username : give account a password
* userdel [-r] username: deletes the account, option r removes the home directory, also removes the user's mail spool file if it exists
* usermod [options] username
* groups username: displays the group the an account belongs to, without supplying username it displays your groups
* group add [options] groupname: creates a new group
    * -g: specify the groupid

* groupdel groupname: deletes the group 
* groupmod [options] groupname: modifies the group
    * -g gid
    * -n newname
* newgrp groupname: changes the users group 

### Networking
* ip address: displays ip information about the machine
* ifconfig: displays ip information about the machine 
* $hostname, $uname -n, $hostname -f : displays the hostname and full qualified domain name witht he f option
* echo 'hostname' > /etc/hostname: changes the hostname persists
* vi /etc/sysconfig/network: makes the hostname persist logins
* hostname 'hostname': changes the hostname of the machine
* hosts: files dns : changes the search from dns first
* ip address add ip[/NETMASK] dev NETWORK_DEVICE: used to manually assign an ip address to a machine
* ip link set eth0 up : brings the interface up 
* ifconfig NETWORK_DEVICE addr network SUBNET_MASK: also used to assign an ip address manually 
* ifconfig networkdevice up : brings the interface up
* ifup/ifdown network_device: used to test the configuration
* ping [-c count] host: when you're having difficulty connecting to a host using the -c options specifies the number of packets to send to the host
* traceroute -n ipaddress: shows the route of the to reaching a host
* tracepath -n ipaddress: an alternative to traceroute
#### special user permissions
* chmod u+s /path/to/file: adds setuid attribute to file
* chmod 4777 /path/to/file: adds setuid attribute with some additional permissons
* chmod u-s /path/to/file: removes setuid attribute to file
* chmod 0777 /path/to/file: removes the setuid attribute to the file
* find / -perm /4000 -ls : finds all the files with the setuid attribute
* find / -perm +4000 -ls : older style for doing the above 
* find / -perm /2000 -ls : finds all the files with the setuid attribute
* find / -perm +2000 -ls : older style for doing the above 
* chmod g+s /path/to/file: adds setgid attribute to file
* chmod 2755 /path/to/file: adds setgid attribute with some additional permissons
* chmod ug+s /path/to/file: adds setgid and setuid attribute to file
* chmod 6755 /path/to/file: adds setgid and setuid attribute with some additional permissons
* chmod g-s /path/to/file: removes setgid attribute to file
* chmod 0755 /path/to/file: removes the setgid attribute to the file








