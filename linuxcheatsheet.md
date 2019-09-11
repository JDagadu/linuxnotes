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
*chgrp [groupname][filename]: change the group the file or folder belongs
* find [directory] [-name|iname|-type|-size|-time|-newer] pattern: used to search for files or folders that match a specific pattern
* locate [pattern]: searches the index for files and folders that matches the pattern

### Vi editor commands
* vi [filename]: enters the vi edit mode
* hjkl: are used to move up left right character by character
* bw: are used to move left and right word by word
* ^$: go to the beginning and end of a line
*iI: to insert at the current cursor position or at the beginning of the line
*aA: to insert text after the cursor position or at the end of the line
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
cp sourcefile1[...sourcefileN] destinationdir: copies the list of files to the destinantion dir
cp -i: run in interactive mode
cp -r source directory destination_dir: copies source directory into destination directory, if the destination directory doesn't exist it creates it
* mv [-i] source destination: moves file from the source to the destination 
* sort file: sorts text as appears in the file alphabetically 
* sort -r: sorts in reverse order
* sort -u: removes duplicates
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
crontab -r: remove all of your cron jobs
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






