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
Implicit Directory Entries
`.` (Current Directory):

Represents the directory you are currently in.
Using . in a path does not change the location; it essentially points to the same directory.
`..` (Parent Directory):

Represents the directory one level up from the current directory.
It is used to navigate upwards in the directory structure.
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


  


