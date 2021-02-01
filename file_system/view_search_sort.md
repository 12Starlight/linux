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

Here are some other ways to view file contents:

&nbsp;

| Command              | Description |
|:---------------------|:------------|
| `tac <path/to/file>`  | Print a file's contents to standard output, reversed vertically. |
| `rev <path/to/file>`  | Print a file's content to standard output, reversed horizontally (along rows). |
| `head -n 15 <path/to/file>`  | Read the first 15 lines from a file (10 by default if -n option not provided.)  |
| `tail -n 15 <path/to/file>`  | Read the bottom 15 lines from a file (10 by default if -n options not provided). |

