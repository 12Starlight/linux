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

*<bold>`NB:`</bold> Redirection breaks pipelines*