# **Aliases**

&nbsp;

Aliases allow you to save your pipelines and commands with easy to remember nicknames
so that they can be used later much easier.

You defined aliases in your **.bash_aliases** file in your home directory. If it does not
exist, you need to create it spelled `exactly` as shown. Note that the preceding (.) must
be included and there should be no file extension (such as .txt, or .pdf).

Here is how you define an alias in **.bash_aliases**:

&nbsp;&nbsp;&nbsp;&nbsp; <kbd>alias</kbd> `alias_name`='THING YOU WANT TO ALIAS'

&nbsp;

Notice that there are no spaces between the equals sign (=) and the alias_name and the
quotes ('). The quotes can be double quote (") or single quotes (').

Let us take an example:

&nbsp;&nbsp;&nbsp;&nbsp; <kbd>alias</kbd> `cal_magic`='<kbd>cal</kbd> `-A` 1 `-B` 1 12 2021'

&nbsp;

With this alias defined in our **.bash_aliases** file, whenever we run the cal_magic command it
is as if we ran the <kbd>cal</kbd> `-A` 1 `-B` 1 12 2021 command.

cal_magic is now said to be an `alias` of '<kbd>cal</kbd> `-A` 1 `-B` 1 12 2021'.

*`NB:` Aliases may contain either one command or an entire pipeline!*