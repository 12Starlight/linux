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

| Command             | Description                                                               |
|:--------------------|:---------------------------------------------------------------------------|
| `Locate -S`         | Print information about the databse file. |
| `sudo updatedb`     | Update the database. As the `updatedb` command is an administrator command, the `sudo` command is used to run `updatedb` as the `root` user (the administrator). |
| `Locate --existing` | Check whether a result actually exists before returning it. |
| `locate -limit 5`   | Limit the output to only show 5 results. |

&nbsp;

# **The Find Command**

The `find` command can be used for more `sophisticated search tasks` than the `locate` command. This is made possible due to the many powerful options that the `find` command has.

The first thing to not is that the `find` command will list both files *and* directories, below the
point the file tree that it is told to start at.

For example:

&nbsp; &nbsp; &nbsp; &nbsp; `find .`

will list all files and directories below the current working directory (which is denoted by the `.`).

&nbsp; &nbsp; &nbsp; &nbsp; `find /`

will list all files and directories below the base directory (`/`); thereby listing everything on the entire file system!

By default, the `find` command will list everything on the file system below its starting point, to an `infinite depth`.

The search depth can however be limited using the `-maxdepth` option.

For example:

&nbsp; &nbsp; &nbsp; &nbsp; `find / -maxdepth 4`

will list everything on the file system below the base directory, provided that it is within `4` levels of the base directory.


&nbsp;

| Command | Description                                                                |
|:--------|:---------------------------------------------------------------------------|
| `Locate -S` | Print information about the databse file. |