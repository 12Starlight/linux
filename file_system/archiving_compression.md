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

| Option | Description |
|:-------|:------------|
| `-c` : "create" | This allows us to create a tarball. (required) |
| `-v` : "verbose" | This makes tar give us feedback on its progress. (optional) |
| `-f` | Tells tar that the next argument is the name of the tarball. (required) |
| `<name_of_tarball>` | The absolute or relative file path to where you want the tarball to be placed; e.g. ~/Desktop/myarchive.tar. It is recommended that you add `.tar` to your proposed filename for clarity. |
| `<file>` | The absolute or relative file paths to files that you want to insert into the tarball. You can have as many as you want and wildcards are accepted. |

&nbsp;

#### **1.1 Checking a Tarball's Contents**

Once the tarball has been created, you can check what is inside it using the tar command.

        tar -tf <name_of_tarball>

&nbsp;

| Option | Description |
|:-------|:------------|
| `-t` : "test-label" | This allows us to check the contents of a tarball. (required) |
| `-f` | Tells tar that the next argument is the name of the tarball. (required) |
| `<name_of_tarball>` | The absolute or relative file path to where you want the tarball to be placed; e.g. ~/Desktop/myarchive.tar |

&nbsp;

#### **1.2 Extracting from a Tarball**

Let us say that you download a tar file from the internet and you want to extract its contents using the command line. How can you do that?

For this you would again use the `tar` command.

        tar -xvf <name_of_tarball>

&nbsp;

| Option | Description |
|:-------|:------------|
| `-x` : "extract" | This allows us to extract a tarball's contents. (required) |
| `-v` : "verbose" | This makes tar give us feedback on its progress. (optional) |
| `-f` | Tells tar that the next argument is the name of the tarball. (required) |
| `<name_of_tarball>` | The absolute or relative file path to where you want the tarball to be placed; e.g. ~/Desktop/myarchive.tar |

&nbsp;

Extracting a tarball does **not** empty the tarball. You can extract from a tarball as many times as you want without affecting the tarball's contents.

&nbsp;

## **2. Compressing Tarballs**

Tarballs are just containers for files. They do not by themselves do any compression, but can be compressed using a variety of compression algorithms.