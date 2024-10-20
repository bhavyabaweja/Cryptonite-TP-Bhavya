## Changing file ownership
`chown` (change owner) command helps changing the file ownership. <br>
Two important user account:
1. Root- administrative account
2. Hacker- user account
**Solution:** <br>
`chown hacker /flag` <br>
`cat /flag`
## Groups and Files 
Files have both owning users and group. A group can have multiple users in it and a user can be a part of multiple groups.<br>
You can check what groups you are a part of using `id` command. <br>
`chgrp` changes the group that owns the file.<br>
**Solution:** <br> 
`chgrp hacker /flag` <br>
`cat /flag`
## Fun with group names 
`id`<br>
`chgrp grp23019` <br>
`chgrp grp23019 /flag` <br> 
`cat /flag`
## Changing Permissions 
`chmod` command is used for changing properties. <br>
`chmod [-options] MODE file_name`

r - user/group/other can read the file (or list the directory)
w - user/group/other can modify the files (or create/delete files in the directory)
x - user/group/other can execute the file as a program (or can enter the directory, e.g., using cd)
- - nothing
**Solution:** <br>
`chmod o+r /flag`<br>
`cat /flag` <br>

`o+r` means giving all other users permission to read the file. <br>
## Executable Files 
Make a file executable for all. <br> 
**Solution:** <br>
`chmod a+x /challenge/run`<br>
`/challenge/run`<br>
## Permission Tweaking Practice 
After changing permissions 8 times in a row, flag was provided. <br>

To modify the permissions of /challenge/pwn from the current permissions `rw-r--r--` to the needed permissions `rw-rwxr--`, you need to adjust the following:

User permissions: No changes needed (already rw-).<br>
Group permissions: Add write (w) and execute (x) permissions to the group.<br>
World (others) permissions: No changes needed (already r--).<br>
To achieve this, you can use the `chmod` command. Specifically, you need to add write and execute permissions for the group (g+wx).<br>
## Permissions Setting Practice 
`chmod` can also simply set permissions altogether, overwriting the old ones. This is done by using `=` instead of `-` or `+`.<br>
Rest it was same as previous question
## The SUID Bit 
The "Set User ID" (SUID) permissions bit allows the user to run a program as the owner of that program's file.<br>
As the owner of a file, you can set a file's SUID bit by using chmod:

`chmod u+s [program]`
**Solution:** <br> 
` chmod u+s /challenge/getroot`<br>
`/challenge/getroot `<br>
`cat /flag `<br>




