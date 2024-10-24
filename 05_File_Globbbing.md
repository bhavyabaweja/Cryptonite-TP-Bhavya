# File Globbing 
## Matching with *
When * is encountered the shell treats it as a wildcard and replaces it the files of matching pattern 
**Solution:**
`cd /ch*`
`/challenge/run `
## Matching with ?
the `?` only matches with a single character 
` cd /?ha??enge `
` /challenge/run`
## Matching with []
[] are a limited form of `?`. They find the characters specified witin the square brackets only.
**Solution:**
`cd /challenge/files `
`/challenge/run file_[absh]`
## Matching paths with []
**Solution:** 
`/challenge/run /challenge/files/file_[absh]`
## Mixing Globs 
**Solution:**
`cd /challenge/files`
`/challenge/run [cep]*`
In `[cep]` c helps in finding word beginning with c i.e. challenging. Similarly, e for educational and p for pwning. 
## Exclusionary Globbing 
`!` acts like a NOT like in other programming languages only when it is the first character inside the square brackets. While `^` is not limited to this case but it does not work with older version of shells.
**Solution:**
`cd /challenge/files`
` /challenge/run [!pwn]*`




