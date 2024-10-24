## Printing Variables 
You can print the variable using `echo` command prepending the variable with `$`.<br>
**Solution:** <br>
`echo $FLAG`
## Setting Variables 
You can set variables using the format `VAR=value`. Don't provide any space in between. `$` is only prepended to acccess variables.<br>
**Solution:** <br>
`PWN=college`
## Multi-word Variables 
Use double quotes if the variable has multiple values(provide spaces between the values).<br>
**Solution:** <br>
`PWN="COLLEGE YEAH"`
## Exporting Variables 
By default a variable is not an environment variable. By using the `export VAR` command you can export the variables.
**Solution:** <br>
`PWN=COLLEGE`<br>
`COLLEGE=PWN` <br>
`export PWN` <br>
`/challenge/run`
## Printing exported variables 
`env` prints every environment variable and their value.Use piping and `grep` to find the output required.<br>
**Solution:** <br>
`env | grep pwn.college`
## Storing output command 
Use the format `VAR=$(command)` to store the output of `command` inside the variable `VAR`.
**Solution:** <br>
`PWN=$(/challenge/run)`
## Reading input 
`read` builtin takes input from user and stores it in variable.(like you use scanf in C). `-p` helps to specify the prompt.Otherwise it would be difficult to understand which is input and which is output.<br>
FORMAT: `read -p "prompt" VAR_NAME`
**Solution:** <br>
`read -p "INPUT: " PWN `<br>
`INPUT: COLLEGE`
## Reading Files
`read` is also used to read entire files into a variable using stdin operator(`<`).<br>
**Solution:** <br>
`read PWN < /challenge/read_me`


