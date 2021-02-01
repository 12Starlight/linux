# **The Locate Command**

The `locate` command searches a `database` on your file system for the files that match
the text (or regular expression) that you provide it as a command line argument.

&nbsp; &nbsp; &nbsp; &nbsp; If results are found, the locate command will return the 
`absolute path` to all matching files.

For example:

&nbsp; &nbsp; &nbsp; &nbsp; `locate` *.txt

will find all files with filenames ending in `.txt` that are registered in the database.

The locate command is fast, but bc it relies on a database it can be error prone if the
database is not kept up to date.

Below are some commands to update the database and some reassuring procedures in case
one cannot access administrator privileges.


&nbsp;

# **The Find Command**