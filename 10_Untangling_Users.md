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
**Solution:** <br>
``<br>
``<br>
``<br>

