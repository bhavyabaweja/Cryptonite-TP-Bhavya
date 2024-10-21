## The PATH Variable 
There is a special shell variable, called PATH, that stores a bunch of directory paths in which the shell will search for programs corresponding to commands.

Without PATH, commands (like `ls`, `cd`, etc ) wont work.
**Solution:** <br>
` PATH=""`<br>
`/challenge/run`<br>
## Setting PATH 
**Solution:** <br>
` PATH=/challenge/more_commands/` <br>
`/challenge/run` <br>
## Adding Commands 
**Solution:** <br>
hacker@path~adding-commands:~$ nano win
hacker@path~adding-commands:~$ cat win
cat /flag

`hacker@path~adding-commands:~$ chmod +x win <br>
hacker@path~adding-commands:~$ echo $PATH
/nix/store/3v4hdb2gmpj7jv2z848ikakhzl9rjgwh-code-server/libexec/code-server/lib/vscode/bin/remote-cli:/run/challenge/bin:/run/workspace/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
hacker@path~adding-commands:~$ PATH=$PATH:/home/hacker
hacker@path~adding-commands:~$ echo $PATH
/nix/store/3v4hdb2gmpj7jv2z848ikakhzl9rjgwh-code-server/libexec/code-server/lib/vscode/bin/remote-cli:/run/challenge/bin:/run/workspace/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/home/hacker
hacker@path~adding-commands:~$ /challenge/run
Invoking 'win'....
pwn.college{AUAPy6vefK7TJfjpzt_SBJn0UA2.dZzNyUDLyEDN1czW}`


