# **Command Structure**

## **Definitions**

&nbsp;

#### **Command**

  * An instruction typed in the terminal and submitted to the shell for interpretation.


#### **Shell**

  * A program that interprets commands for meaning.


#### **Terminal**

  * A graphical window where commands can be typed and submitted to the shell.

&nbsp;

## **Command Structure**

Each command follows the same overarching structure:

&nbsp;&nbsp;&nbsp;&nbsp;  <kbd>command_name</kbd> `-options` <mark>arguments</mark>

&nbsp;

#### **Command Names**

<kbd>command_name</kbd> must be a valid program on the Shell's Path. To check this,
use the which command like so:

&nbsp;&nbsp;&nbsp;&nbsp;  <kbd>which</kbd> `command_name`

&nbsp;

If a path is returned, then the <kbd>command_name</kbd> is valid and vise versa.

&nbsp;

#### **Options**

You can specify options for each command to customize the commands behavior. These
can be either 'short-form' options or 'long-form' options.

Each command behaves differently so check the command's manual <kbd>man</kbd> page
for the specifics of each command's behaviour.

&nbsp;

#### *Short Form Options*

Short-form options are where a letter defines an option. Each option is prepended by
a dash "-" like so:

&nbsp;&nbsp;&nbsp;&nbsp;  <kbd>command_name</kbd> `-a -b -c` <mark>args</mark>

&nbsp;

To save typing, you could join together the options:

&nbsp;&nbsp;&nbsp;&nbsp;  <kbd>command_name</kbd> `-abc` <mark>args</mark>

&nbsp;

Both of these formats are equivalent.

&nbsp;

#### *Long Form Options*

For some commands, there are long-form options defined to make options easier to identify.
Longform options are usually prepended by a double dash "_".

Long-form options **cannot** be joined together like short-form options can.

Whether they are defined or not depends on each specific command, so consult the command's
manual page for more information.

If long form options are defined for options 'a', 'b', 'c', then:

&nbsp;&nbsp;&nbsp;&nbsp;  <kbd>command_name</kbd> `-a -b -c` <mark>arguments</mark>

&nbsp;

is eqivalent to

&nbsp;&nbsp;&nbsp;&nbsp;  <kbd>command_name</kbd> `--alpha --beta --charlie` <mark>arguments</mark>

&nbsp;

#### **Command Line Arguments**

<mark>command_line_arguments</mark> are a type of input that commands operate on.

Some commands can take an unlimited amount of inputs, some take a specific amount, and
some take none at all. Consult the manual page for the specific command for more 
information.

&nbsp;&nbsp;&nbsp;&nbsp;  <kbd>cal</kbd> <mark>12</mark> <mark>2017</mark>

&nbsp;

Here the <kbd>cal</kbd> command has <mark>2_command_line_arguments</mark>. The number
<mark>12</mark> and the number <mark>2017</mark>.

&nbsp;

#### *Arguments For Options*

Sometimes, command options can also take their own arguments (inputs).

&nbsp;&nbsp;&nbsp;&nbsp;  <kbd>cal</kbd> `-A` <mark>1</mark> `-B` <mark>1</mark> <mark>12</mark> <mark>2017</mark>

&nbsp;

Here the <kbd>cal</kbd> command has `2 options`; `A` and `B`.

The `A option` has its own argument (<mark>1</mark>).

The `B options` has its own argument (<mark>1</mark>).

And the <kbd>cal</kbd> command has <mark>2 command line argument</mark>(<mark>12</mark> <mark>2017</mark>).

&nbsp;

## **Using the Manual**

<kbd>man -k [command_name]</kbd> ~ Manual pages for that command_name

<kbd>man [page] [command_name]</kbd> ~ Manual page for that command_name

<kbd>help</kbd> ~ Manual pages for built in Shell commands