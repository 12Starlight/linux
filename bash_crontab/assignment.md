# **Bash Crontab Assignment**

## **1).**
In this task you are asked to create a bash script called <kbd>hungry.sh</kbd> in your home directory.

<kbd>hungry.sh</kbd> should do two things:

Firstly, it should output the text `I am hungry. Feed me data.` to a file in your desktop directory
called <kbd>demands.txt</kbd>

Secondly, <kbd>hungry.sh</kbd> should also output the date and time that the demand was made to a file in your desktop directory called <kbd>demands.log</kbd>

Do ensure that each output is *appended* to the previous one.

**Hint:** Ensure that the bash script starts with the required `#!/bin/bash` text

&nbsp;

> Answer:
>
> cd ~
>
> mkdir /bin
>
> cd /bin
>
> nano hungry.sh
>
> #!/bin/bash
>
> echo "I am hungry. Feed me data" >> ~/Desktop/demands.txt
>
> date >> ~/Desktop/demands.log
>
> ctr + o
>
> ctr + x


