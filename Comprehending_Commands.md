# Comprehending Commands
## cat: not the pet,but the command
cat reads out files.

cat will concatenate multiple files if given multiple arguments.

## catting absolute paths
**Solution:**
`cat /flag`
## more catting practice
**Solution:**
`cat /usr/share/misc/flag`
## grepping for a needle in haystack
when files are too big to `cat` then use `grep` to search for content
**Solution:**
`grep pwn.college /challenge/data.txt`
grep finds pwn.college in the path `/challenge/data.txt`
## listing files
ls will list files in all the directories provided to it as arguments.

**Solution:**
`ls /challenge`
`/challenge/7997-renamed-run-6089`
## touching files
you can create blank new files using `touch` command
**Solution:**
`cd /tmp`
``touch pwn`
`ls`
`touch college`
`ls`
`/challenge/run`

`ls` is used for listing all the files in a directory.
## removing files
use `rm` command to remove files
**Solution:**
`ls`
`rm delete_me`
`ls`
`/challenge/check`
## hidden files 
`ls` doesn't list all files by default. files starting with `.` in Linus don't show up using `ls` command so for that use `ls -a` command.

**Solution:**
`cd /`
`ls`
`ls -a`
`cat .flag-68602747427006`
## An epic filesystem quest 
This was a game where i had to enter a directory using`cd`. But at times i had to get the access of directory files without `cd`ing into it otherwise the next clue will get self destroyed. So in that case i used `cat` to read the contents in directory without `cd`ing into it.
## Making directories 
directories can be made using `mkdir` command.
**Solution:**
`cd /tmp`
`mkdir pwn`
`cd /tmp/pwn`
``touch college`
`ls`
`/challenge/run`
## Finding Files 
use `find` command to find the files 
`-type` tells the type of directory or file to be found 
**Solution:**
`find / -name flag -type f`
`cat /opt/linux/linux-5.4/arch/xtensa/variants/dc232b/include/flag`
## Linking files 
Symbolic link is a link that is used to point to other files or directories(folders).

A soft link or symbolic link points to original file on system. 

A hard link creats a copy of the file.

**Solution:** <br>
`ln -s /flag /home/hacker/not-the-flag`
/home/hacker/not-the-flag is the symlink

You use the ln command to create the links for the files and the -s option to specify that this will be a symbolic link. If you omit the -s option, then a hard link will be created instead.




