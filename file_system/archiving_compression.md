# **File Archiving and Compression**

File archiving and compression is a `two-step` process in Linux.

First one creates a `tarball` to hold all the files that comprise the archive, and then
compresses that tarball using one of a variety of `compression` algorithms.

&nbsp;

## **The Overall Process**

&nbsp; &nbsp; &nbsp; &nbsp; **`1) Create a Tarball`**

&nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; First, you will create what is known as a tar file or "`tarball`". A tarball is a way of 

&nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; bundling together the files that you want to archive.

&nbsp;

&nbsp; &nbsp; &nbsp; &nbsp; **`2) Compress the Tarball`**

&nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; Secondly, you will then compress the tarball with one of a variety of compression algorithms; 

&nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; leaving you with a compressed archive.

&nbsp;

## **1. Creating a Tarball**

Tarballs are created using the `tar` command.

        tar -cvf <name_of_tarball> <file>...

&nbsp;

`The -c option`: "create". This allows us to create a tarball. (required)

`The -v option`: "verbose". This makes tar give us feedback on its progress. (optional)

`The -f option`: Tells tar that the next argument is the name of the tarball. (required)

`<name_of_tarball>`: The absolute or relative file path to where you want the tarball to be placed;
e.g. ~/Desktop/myarchive.tar. It is recommended that you add .tar to your proposed filename for clarity.

`<file>`: The absolute or relative file paths to files that you want to insert into the tarball. You can have as many as you want and wildcards are accepted.