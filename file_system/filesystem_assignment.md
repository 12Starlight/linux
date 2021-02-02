# **File System Assignment**

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