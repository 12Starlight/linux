# **Viewing File Content**

There exist commands to open files and print their content to standard output. One such
example is the `cat` command. Let us say we have a file called `hello.txt` on the Desktop.

By peforming:

&nbsp; &nbsp; &nbsp; &nbsp; `cat` ~/Desktop/hello.txt

This will print out the contents of `hello.txt` to standard output where it can be viewed
or piped other commands if required.

One such command to pipe to would be the less command. The `less` command is known as a
'pager' program and excels at allowing a user to page through large amounts of output in
a more user-friendly manner than just using the terminal.

An example may be:

&nbsp; &nbsp; &nbsp; &nbsp; `cat` ~/Desktop/hello.txt | `less`

Or more simply:

&nbsp; &nbsp; &nbsp; &nbsp; `less` ~/Desktop/hello.txt

By pressing the `q key`, the `less` command can be terminated and control regained over the 
shell.

