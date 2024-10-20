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
## 
