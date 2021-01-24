# **Piping**

&nbsp;

`Piping` is the `connection` of the `standard output` of one command to the `standard input`
of another command. Piping using the `pipe character (|)`. 

&nbsp;

Here is how you would pipe together `command_one` and `command_two`:

&nbsp;&nbsp;&nbsp;&nbsp; <kbd>command_one</kbd> `-options` <mark>arguments</mark> | <kbd>command_two</kbd> `-options` <mark>arguments</mark>

&nbsp;

Notice how both commands can have their own options and command line arguments as usual.
This piping can go on for as long as is required with as many commands as is required.

&nbsp;

## **Taking `Snapshots` of pipeline data using the tee command**

&nbsp;

Redirecting during a pipeline breaks the pipeline.

For example, this **wouldn't** work:

&nbsp;&nbsp;&nbsp;&nbsp; <kbd>command_one</kbd> `-options` <mark>arguments</mark> > snapshot.txt | <kbd>command_two</kbd> `-options` <mark>arguments</mark>

&nbsp;

Because redirection is processed by the shell before piping is, snapshot.txt would be created,
but this locks up the standard output stream and therefore no data can be passed through the
pipeline to `command_two`. 

*`NB:` Redirection breaks pipelines*

&nbsp;

However, the <kbd>tee</kbd> command allows us to take a 'snapshot' of the data in the pipeline
**without** breaking the pipeline.

&nbsp;&nbsp;&nbsp;&nbsp; <kbd>command_one</kbd> `-options` <mark>arguments</mark> | tee snapshot.txt | <kbd>command_two</kbd> `-options` <mark>arguments</mark>

&nbsp;

Here, a snapshot of the data coming out of `command_one` is saved in snapshot.txt, but the data is 
also successfully piped through to `command-two`.

&nbsp;

## **Piping to commands that only accept command line arguments by using xargs**

&nbsp;

Piping connects the `standard output` of one command to the `standard input` of another command.

But what if the second commande doesn't accept standard input? e.g. the <kbd>echo</kbd> command.

The key is to transform the data comming in, into command line arguments.

This is possible using the `xargs` command.

For example, this would **not** work:

&nbsp;&nbsp;&nbsp;&nbsp; <kbd>command_one</kbd> `-options` <mark>arguments</mark> | echo

&nbsp;

This **would** work:

&nbsp;&nbsp;&nbsp;&nbsp; <kbd>command_one</kbd> `-options` <mark>arguments</mark> | <kbd>xargs</kbd> echo
