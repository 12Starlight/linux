# **File System Assignment**

**1)**
In this task you are asked to create a folder called `super_secret_stuff` and inside that folder to
place a file called <kbd>top_secret.txt</kbd>

<kbd>top_secret.txt</kbd> may contain whatever content you wish.

Once you have created the file, use the `updatedb` command and the `locate` command to find
the path to <kbd>top_secret.txt</kbd>.

Using redirection, save the path that the `locate` command gives you to a new file called
<kbd>secret_place.txt</kbd> in your home directory.

**Hint: You will need to use sudo to gain the elevated privileges required to update the
database.**

&nbsp;

> Answer: 
> 
> mkdir super_secret_stuff
>
> touch super_secret_stuff/top_secret.txt
>
> nano super_secret_stuff/top_secret.txt
>
> Typed: 'This is the best Linux course ever!
>
> ctr + o
>
> ctr + x
>
> sudo updatedb
>
> locate top_secret.txt
>
> locate top_secret.txt > ~/secret_place.txt 


&nbsp;

**2)**

`Part A`:


In this task, you are going to create an advanced pipeline that will create a sorted list of
the various file sizes on your system.

Firstly, use the `find` command to search your entire file tree; starting from the `/`
directory, for all files that are over 1 MebiByte in size. Use the `maxdepth` option to limit
the `find` command’s search to only go 4 levels deep. The search should only show
files, not directories.

Use the `-exec` option of the `find` command to run the `ls -lh` command on each of
those results.

**Hint: You will need to put sudo at the start of this command to access all required
folders.**

> Answer:
>
> sudo find / -maxdepth 4 -type f -size +1M -exec ls -lh \;

&nbsp;

`Part B`:

Sort the output from Part A using the `sort` command. You should sort the data so that
the largest file sizes are at the top of the list and the smallest file sizes are at the bottom.

Using redirection, output this data to a file called <kbd>filesizes.txt</kbd> in your home directory.

**Hint 1:** You will need to use the `–k` option for the sort command and define a
*KEYDEF*.

**Hint 2:** The file sizes are the 5th column of data.

**Hint 3:** You need to let the sort command to be able to deal with “human-readable”
data.

> Answer:
>
> sudo find / -maxdepth 4 -type f -size +1M -exec ls -lh \; | sort -k 5hr > ~/Desktop/filesizes.txt

&nbsp;

> Reviewed:
>
> sudo find / -maxdepth 4 -type f -size +1M -exec ls -lh `{}` \; | sort -k 5hr > ~/Desktop/filesizes.txt