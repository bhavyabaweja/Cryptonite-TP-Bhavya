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
`ctrl+z` is used to suspends process without terminating it.
**Solution:** <br>
`/challenge/run` <br>
`ctrl+z` <br>
`/challenge/run`
## Resuming Processes 
`fg` is used to resume a suspended process and bring it to foreground. <br>
**Solution:** <br>
`/challenge/run` <br>
`ctrl+z` <br>
`fg /challenge/run`
## Backgrounding Processes 
Processes can be resumed in background using `bg` command. <br>
**Solution:** <br>
`/challenge/run` <br>
`ctrl+z` <br>
`bg /challenge/run` <br>
`/challenge/run`
## Foregrounding Processes 
`fg` can also foreground a backgrouded process.<br>
**Solution:** <br>
`/challenge/run` <br>
`ctrl+z` <br>
`bg /challenge/run` <br>
`fg /challenge/run`
## Starting Background Processes 
Append `&` to start background process. <br>
The process will run in background.<br>
**Solution:** <br>
`/challenge/run &` <br>
## Process Exit Codes 
The process is finished using exit code. This exit code is crucial for determining whether the process completed successfully or encountered an error. `0` implies that the process ran successully and `1` or any other value indicates that there was some error.<br>
Exit code of most recently terminated process can be checked using `$?`.<br>
**Solution:** <br>
`/challenge/get-code` <br>
`echo $?` <br>
`/challenge/submit_code 229` 







