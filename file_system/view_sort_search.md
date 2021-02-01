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

&nbsp;

# **Sorting Data**

A useful ability when working with file data is to be able to sort it either alphabetically or
numerically. This behavior is handled using the `sort` command.

By default, the sort command sorts `smallest first`. So if sorting alphabetically, it will be
default sort from from a - z. If sorting numerically, it will put the smallest numbers first,
and the largest last.

Here are some common options when using the sort command:

&nbsp;

| Command | Description |
|:----------|:------------|
| `sort -r` | Reverse the default sorting order. |
| `sort -n` | Sort in a numerical manner. |
| `sort -u` | Sort data and only return unique entries. |

&nbsp;

It is also possible to sort tabular data using the `sort` command using one of the columns. This
is posiible by providing a `KEYDEF` as an argument to the `-k` option.

&nbsp; &nbsp; &nbsp; &nbsp; `sort -k <KEYDEF>`

KEYDEFS are made using a column number and then additional options can be added (without dashes).

As and example:

&nbsp; &nbsp; &nbsp; &nbsp; `sort -k 5nr`

The `KEYDEF` is `5nr`. This will sort using column `5` of the data, and sort numerically (`-n option`) but in reverse (`-r option`).

&nbsp;

# **Searching File Contents**

The ability to search for and filter out what you want from a file or standard output makes working
with the command line a much more efficient process. 

The command for this is called the `grep` command. 

The `grep` command will return all lines that match the particular piece of text (or regular expression) provided as a search term.

For example:

&nbsp; &nbsp; &nbsp; &nbsp; `grep` hello myfile.txt 

Will return all lines containing the word "hello" in myfile.txt

and

&nbsp; &nbsp; &nbsp; &nbsp; `ls` /etc | `grep` *.conf

will return all lines with anything ending in ".conf" in data piped from the `ls` command.
Some common options when working with the `grep` command include:

&nbsp;

| Command | Description |
|:--------|:------------|
