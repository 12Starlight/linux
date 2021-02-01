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