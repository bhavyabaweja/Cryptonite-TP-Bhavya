# Comprehending Commands
## cat: not the pet,but the command
cat reads out files.

cat will concatenate multiple files if given multiple arguments.

## catting absolute paths
**Solution:**
`cat /flag`
## more catting practice
**Solution:**
`cat /usr/share/misc/flag`
## grepping for a needle in haystack
when files are too big to `cat` then use `grep` to search for content
**Solution:**
`grep pwn.college /challenge/data.txt`
grep finds pwn.college in the path `/challenge/data.txt`
## listing files
ls will list files in all the directories provided to it as arguments.

**Solution:**
`ls /challenge`
`/challenge/7997-renamed-run-6089`
## touching files
you can create blank new files using `touch` command


