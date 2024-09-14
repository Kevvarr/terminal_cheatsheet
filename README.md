# ubuntuCMD
Some basic/intermediate/advance commands for Ubuntu Linux

# Basic
pwd:  prints current address
/home/kevin
- clear: clear cli
- ls: list of directories and files
- ls -al: Shows "rights user group diskSize dateInit" / hidden are also included with -a / -l not hidden
- cd: move between directories / cd .. exit current directory
- touch: create a file
- cp <file1> <file1Copy>: copy files
- mv: move files or directories, or even renaming then
- rm: removes files / rm -r: Remove directories, empty or not
- mkdir: creates Directories
- rmdir: removes Empty Directories
- man: provides help with a command
- ">" : (override) redirects information from left to the right eg. date > file.txt
- ">>" : (append) redirects information from left to the right eg. date > file.txt
- cat: shows entire file
- cat: shows 10 lines of file
- cat: shows last 10 lines of the file
- cat: or contatenate in output
- sort: sort the output
# Intermediate
- su: changes user
- sudo: run commands with elevated permissions (root)
- nano: editor
- ps: process status
- kill <PID>: kill (terminates) programs
- |: pipelines
- diff: Shows difference between files
- find: find files or folders by patterns
- grep: find text inside files
- top: shows more cpu intensive process
- jobs: shows jobs
- bg: rusmes job in background (&)
- fg: resumes job in foreground
- gzip: compresses files to zip (-k to save the file copy)
- gunzip: unzip
- tar: create an archive, grouping multiple files in a single file
- ln: create links (hard link) -> like a pointer to another file
- ln -s: create links (soft link) -> like a pointer to another file
- chown: changes ownership of a file/directory
- chmod: changes permisions in a file/directory

# Advance
- man: provides help about command
- shutdown -h now: shutdown machine now (-r to restart instead of -h)
- head/tail: shows first/last 10 lines
- uname: shows kernel info
- sudo ss -ltn: check open ports
- netstat: also check open ports (old way)
- ifconfig: check ip address
- ip addr show: also checks ip address
- df -ah:checks for free disk space
- systemctl: Manages a service
- systemd: (new way) Manages a service such as nginx, mysql...
- du -sh : Check size in a directory's content
- ps aux | grepn <process>: Checks cpu usage of a process
