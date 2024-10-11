# Practicing Piping 
## Redirecting Output 
`stdout` can be used with `>` operator 

**Solution:** 
`echo PWN > COLLEGE`
``

The output of `echo PWN` which will be PWN will be redirected to file named COLLEGE
## Redirecting more output 
The output of any command can be redirected apart from `echo`.

The ouput of `/challenge/run` needs to be redirected to `myflag`.

**Solution:**
`/challenge/run > myflag`

`cat myflag`
## Appending output 
You can redirect input in append mode using `>>` instead of `>`<br>
`>` would delete the previous output when new output comes.


