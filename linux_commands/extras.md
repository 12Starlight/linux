# **command_name options inputs**

command_name ~ Program Name

<kbd>echo `$`PATH</kbd> ~ Lets you see the Shell path

Shell Path ~ List of folders that contain these programs

<kbd>which [command_name]</kbd> ~ Tells which directory the command_name is stored in

&nbsp;

Some command_name's do require an input also known as an operand bc some commands
operate on the input

Options are presided by <kbd>-a</kbd>, <kbd>-b</kbd>, <kbd>-c</kbd>, <kbd>-d</kbd>
<kbd>-e</kbd>, <kbd>-f</kbd>, <kbd>-g</kbd> or you can chain the commands together
<kbd>-abcdefg</kbd>

Long form options are presided by <kbd>--two_dashes</kbd> and can not be chained. 
So, in long form it would be <kbd>--opt_1</kbd>, <kbd>--opt_2</kbd>, <kbd>--opt_3</kbd>

command_name and options are capital sensitive and need to be spelled exactly 

Sometimes options have their own inputs

<kbd>></kbd> ~ Write into a file by first truncating the contents of the previous content

<kbd>>></kbd> ~ Write into a file by appending to the previous data in that file

<kbd>|</kbd> ~ Piping takes the output from one command and uses it as the input in another command

The Shell processes redirections before pipes, so having a redirection before a pipe will break a pipeline

<kbd>tee</kbd> ~ Allows the data stream to flow down 

<kbd>xargs</kbd> ~ For commands that do not accept STDIN, changes STDIN to an argument that can be used with that command

Commands that use xargs can still have their own arguments




&nbsp;

### **Going to be re-written shortly**