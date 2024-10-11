# Pondering Paths
Linux filesystem is a tree. Each directory can contain subsequent directories and files.
## The Root
Invoked the program using path `/pwn` and captured the flag.
#### Absolute Path
Style of path that starts with root directory.
## Program and absolute paths
Path to challenge program 'run': `/challenge/run`
## Position thy self
navigate directory using cd(change directory) command.
~ shows current where shell is located at
When i executed challenge from different directory, it asked me to go to a specific directory using cd.
**Solution:**
`cd /proc/179`
`/challenge/run`
## Position elsewhere 
`cd /usr/share/zoneinfo/posix/Asia`
`/challenge/run`
## Position yet elsewhere 
`cd /var/lib/apt/lists`
`/challenge/run`
## implicit relative paths, from /
#### Relative Path
A relative path is any path that does not start at root (i.e., it does not start with /).
**Solution:**
`cd /`
`challenge/run`
## explicit relative paths, from /
The first, ., refers right to the same directory.<br>
**Solution:**
`cd /`
`./challenge/run`

./challenge/run is a relative path, invoked from the right directory!
## implicit relative path
`pwd` command is used to check for current directory

**Solution:**
`cd /`
`cd challenge`
`./run`
## home sweet home
Expansion of ~ is an absolute path, and only the leading ~ is expanded.<br>
`~/~` will be expanded to `/home/hacker/~` rather than `/home/hacker/home/hacker`
**Solution:**
`/challenge/run ~/x`

  `/challenge/run` is the command and `~/x` is the file specified as argument.


  


