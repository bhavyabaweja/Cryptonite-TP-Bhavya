## Chaining with semicolons 
Commands can be chained using `;`. Isntead of terminating the commands one by one, we can write them in one go using semicolon.
**Solution:** <br>
`/challenge/pwn; /challenge/college` <br>
## Your First Shell Script
Run `/challenge/pwn` and then `/challenge/college`, but this time in a shell script called `x.sh`. <br>
Various text editors can be used such as `vim`. 
**Solution:** <br>
`touch x.sh`<br>
`code x.sh`<br>
Write the commands in x.sh and save it.<br>
`bash x.sh`<br>
## Redirecting Script Output 
Piping (|) from your script to another program. Like before, you need to create a script that calls the /challenge/pwn command followed by the /challenge/college command, and pipe the output of the script into a single invocation of the /challenge/solve command!<br>

