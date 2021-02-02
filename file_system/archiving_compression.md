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

The main types of compression algorithms are `gzip` and `bzip2`.

The `gzip` compression algorithm tends to be faster than `bzip2` but, as a trade-off, `gzip` usually offers less compression.

You can learn more about compression algorithms [here](https://www.rootusers.com/gzip-vs-bzip2-vs-xz-performance-comparison/)

&nbsp;

#### **2.1 Compressing and Decompressing with `gzip`**

| Type | Command |
|:-----|:--------|
| **`Compressing with gzip`** | gzip <name_of_tarball> |
| **`Decompressing with gzip`** | gunzip <name_of_tarball> |

&nbsp;

When compressing with `gzip`, the file extension `.gz` is automatically added to the `.tar` archive. Therefore, the `gzip` compressed tar archive would, by convention, have the file extensions `.tar .gz`

&nbsp;

#### **2.2 Compressing and Decompressing with `bzip2`**

| Type | Command |
|:-----|:--------|
| **`Compressing with bzip2`** | bzip2 <name_of_tarball> |
| **`Decompressing with bzip2`** | bunzip2 <name_of_tarball> |

&nbsp;

When compressing with `bzip2`, the file extension `.bz2` is automatically added to the `.tar` archive. Therefore, the `bzip2` compressed tar archive would, by convention, have the file extensions `.tar .bz2`

&nbsp;

## **Doing it all in one step**

Bc compressing tar archives is such a common function, it is possible to create a tar archive and compress it all in one step using the tar command. It is also possible to decompress and extract a compressed archive in one step using the tar command too.

To perform compression/decompression using gzip compression algorithm in the tar command, you provide the `z` option in addition to the other options required.

| Type | Command |
|:-----|:--------|
| **`Creating a tarball and compressing via gzip`** | `tar -cv[z]f <name_of_tarball><file>...` |
| **`Decomposing a tarball and extracting via gzip`** | `tar -xv[z]f <name_of_tarball>` |

&nbsp;

To perform compression/decompression using bzip2 compression algorithm in the tar commmand, you provide the `j` option to the other options required.

| Type | Command |
|:-----|:--------|
| **`Creating a tarball and compressing via bzip2`** | `tar -cv[j]f <name_of_tarball><file>...` |
| **`Decomposing a tarball and extracting via bzip2`** | `tar -xv[j]f <name_of_tarball>` |

&nbsp;

To perform compression/decompression using the xzip compression algorithm in the tar command, you provide the `J` option to the other options required.

| Type | Command |
|:-----|:--------|
| **`Creating a tarball and compressing via xzip`** | `tar -cv[J]f <name_of_tarball><file>...` |
| **`Decomposing a tarball and extracting via xzip`** | `tar -xv[J]f <name_of_tarball>` |

&nbsp;

## **Creating .zip files**

Although `.tar .gz` and `.tar .bz2` archives are the archives of choice on Linux, `.zip` archives are common on other operating systems such as Windows and Mac OSX.

In order to create such archives, use the following commands:

