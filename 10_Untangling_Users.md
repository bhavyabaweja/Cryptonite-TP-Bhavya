## Becoming root with su 
`su` ( switch user) command <br>
`su` with no arguemnts starts at root shell.<br>
**Solution:** <br>
`su`<br>
`hack-the-planet`<br>
`cat /flag` <br>
## Other users with su
You can give some argument to `su` to switch to that user instead of root. <br>
**Solution:** <br>
`su zardus`<br>
`dont-hack-me`<br>
`/challenge/run`<br>
## Cracking Passwords 
All the passwords are stored in `etc/shadow`. Crack the value of password using hashed value. We have the leak of `/etc/shadow` in this level. 
A value of * or ! functionally means that password login for the account is disabled, a blank field means that there is no password.

Using the command john we can give it the password file as an argument, and it will scan through and decode the password.
**Solution:** <br>
`john /challenge/shadow-leak`<br>
`john --show /challenge/shadow-leak`<br>
`su zardus`<br>
Input Password
`/challenge/run`<br>
## Using sudo 
Unlike su, where you would typically switch to another user (such as root), sudo allows you to execute specific commands with root privileges while still being logged in as your regular user.<br>
**Solution:** <br>
`sudo cat /flag`<br>


