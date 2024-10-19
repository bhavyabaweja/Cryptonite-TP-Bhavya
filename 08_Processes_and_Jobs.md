## Listing processes 
`ps` is used to list running processes(process snapshot or process status).<br>
PID is a number that uniquely identifies every running process.<br>
Two ways to specify arguments:<br>
1. Standard Syntax(`ef`):
   `e` to list every process.<br>
   `f` for full format output.<br>
2. BSD Syntax(`aux`):
   `a` to list processes for all users<br>
   `x` to list processes that are not running in terminal<br>
   `u` for  a user-readable output<br>
**Solution:** <br>
`ps aux`<br>
`/challenge/28957-run-26328`<br>
## Killing processes
`kill` command will terminate a process in a way that gives it a chance to get its affairs in order before ceasing to exist.<br>
Provide the PID from ps as an argument to `kill` a process.<br>
**Solution:** <br>
` ps aux`<br>
` kill 73`<br>
` /challenge/run`
## Interrupting Processes 
`ctrl + c` interrupts whatever process is running and ends it immediately.<br>
**Solution:** <br>
`/challenge/run`<br>
`^C`
## Suspending Processes 

