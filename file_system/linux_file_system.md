# **The Linux File System**

The Linux File System follows a `tree-like` structure starting at a base (or root)
directory, indicated by the slash (`/`).

Locations on the file system are indicated using `file paths`.

Paths that start at the `base directory` (`/`) are known as `absolute paths`.

Paths that start from the `current working directory` of the shell, are know as 
`relative paths`.

For example both of these examples refer to a file called 'file1.txt' in the Documents 
folder fo ra user called Sarah. The relative path assumes the shell is in Sarah's 
home directory.

`Absolute`: /home/sarah/Documents/file1.txt

`Relative`: Documents/file1.txt

&nbsp;

## **Key Commands for Navigating the File System**

|           |                                                                            |
|:----------|:---------------------------------------------------------------------------|
| **`pwd`** | Print on standard output the absolute path to the shell's current working directory. |
| **`cd[<new_location>]`** | Change the shell's current working directory to the optional `<new_location>`. If no location is provided, return to the user's home directory. |
| **`ls[<location>]`** | List out the contents of the optional `<location>` directory. If no `<location>` is provided, print out the contents of the shell's current working directory. | 

&nbsp;

## **Key Shortcuts when Navigating File System.**

|           |                                                                            |
|:----------|:---------------------------------------------------------------------------|
| **`~`**   | The current user's home directory. |
| **`.`**   | The current folder. |
| **`..`**  | The parent directory of the current folder. |