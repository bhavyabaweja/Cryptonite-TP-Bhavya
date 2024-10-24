# Practicing Piping 
## Redirecting Output 
`stdout` can be used with `>` operator 

**Solution:** 
`echo PWN > COLLEGE`

The output of `echo PWN` which will be PWN will be redirected to file named COLLEGE
## Redirecting more output 
The output of any command can be redirected apart from `echo`.

The ouput of `/challenge/run` needs to be redirected to `myflag`.

**Solution:**
`/challenge/run > myflag`

`cat myflag`
## Appending output 
You can redirect input in append mode using `>>` instead of `>`.<br>
`>` would delete the previous output when new output comes.
**Solution:**
`/challenge/run >> /home/hacker/the-flag`<br>
` cat /home/hacker/the-flag`
## Redirecting errors 
Error channel can also be redirected just like the output.<br>
A File Descriptor (FD) is a number the describes a communication channel in Linux. You've already been using them, even though you didn't realize it. We're already familiar with three:

FD 0: Standard Input
FD 1: Standard Output
FD 2: Standard Error

Redirect output of `/challenge/run` to `myflag` and the error to `instructions` files respectively.<br>
**Solution:**
`/challenge/run > myflag 2> instructions`
`cat myflag`
## Redirecting input 
Use `<` to redirect input.<br>
**Solution:** <br>
`echo COLLEGE > PWN ` <br>
` /challenge/run < PWN`
## Grepping stored results
`grep` is used for searching a pattern within various lines of text in a file.<br>
**Solution:** <br>
`/challenge/run > /tmp/data.txt`<br>
`grep pwn /tmp/data.txt`
## Grepping live output
You can cut the process of storing results before grepping using `|`(pipe) operator.<br>
**Solution:** <br>
`/challenge/run | grep pwn `
## Grepping Errors
The `|` operator redirects only standard output to another program, and there is no `2|` form of the operator.<br>
1. Redirect stderr (FD 2) to stdout (FD 1) using `2>&1`. This sends all error messages to the standard output stream.<br>
2. Pipe the combined output to grep to search for the flag.
**Solution:** <br>
`/challenge/run 2>&1 | grep pwn.college`
## Duplicating piped data with tee
The tee command duplicates data flowing through your pipes to any number of files.<br>
**Solution:** <br>
` /challenge/pwn | tee pwn_output | /challenge/college`<br>
` cat pwn_output`<br>
`/challenge/pwn --secret "86beQk0q" | /challenge/college`
## Writing to multiple programs 
**Solution:** <br>
`/challenge/hack | tee >(/challenge/the) >(/challenge/planet)`
## Split-piping stderr and stdout
**Solution:** <br>
`/challenge/hack > >(/challenge/planet) 2> >(/challenge/the)`










