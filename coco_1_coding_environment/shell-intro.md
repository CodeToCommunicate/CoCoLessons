![CoCo logo](https://github.com/CodeToCommunicate/CoCoLessons/blob/main/media/coco-banner.jpg)

# Introduction to the shell

Here, we'll learn about the *shell*,
a command-based interface for interacting
with the operating system of a computer.


## Open a terminal

A *terminal* is an application that allows a user to communicate
with the operating system of a computer
through terse text commands.

* JupyterLab: Terminal app in the Launcher
* Linux: terminal or xterm
* macOS: Terminal.app (built-in) or [iTerm.app](https://www.iterm2.com/) (better)
* Windows: Git Bash Shell in [Git for Windows](https://gitforwindows.org/)

At this time,
if you haven't already done so,
open a terminal.


## Why are we using a terminal?

Because it works. Really well.

When you develop skill with shell commands in a terminal,
you can do filesystem-specific tasks--moving, copying, renaming, deleting
files and directories--much faster than with a graphical application.

By analogy, think of keyboard shortcuts on your computer:
if you want to change from one application to another,
it's much faster to hit `Cmd-Tab` (on macOS; `Alt-Tab` on Linux and Windows)
than it is to use a mouse to go find the other application window.

Commands tend to be terse to the point of being cryptic,
not that different from texting shorthand:
instead of brb or ttyl, it's `cd` or `rm`.
And it's done for the same reason: speed.

Commands can also be gathered into *scripts* that can be executed as a single unit.
With a script, you can automate a repetitive task.
Scripts are marvelous for data processing pipelines,
and can improve reproducibility.
We won't cover scripting here,
but there's more information in Software Carpentry's
[The Unix Shell](https://swcarpentry.github.io/shell-novice/) lesson,
on which this lesson is based.


## Enter commands, get results

The command prompt (or shell prompt) is where we enter commands into a terminal.
It's typically denoted with a dollar sign `$`.

We use a terminal in a **read-evaluate-print loop (REPL)**;
that is, when we enter a command at the prompt, the shell

1. reads the command
1. evaluates the command
1. prints output to the terminal

This process is repeated every time we enter a command.


## Files and directories

Information on a computer is stored in files and directories.
The part of an operating system that handles this information
is called the *filesystem*.
Think of the filesystem as a tree with branches (directories)
and leaves (files).

Let's find out where we are in the filesystem when we start a terminal.
```
$ pwd
/home/jupyter-mpiper
```
The `pwd` command prints the current directory to the terminal.
You can see that I'm in the directory `jupyter-mpiper` under the directory `home`.
The forward slash `/` is used as a delimiter between directory names.

This directory, `/home/jupyter-mpiper`, is special--it's the *home directory*
for the user `jupyter-mpiper`.
Every user has a home directory.
It's the default location for you to create and store information.

Note that I executed this command on a JupyterHub,
which is running Linux;
the home directory on a macOS or Windows machine will be slightly different.


## Directory listings

Next, let's look at the contents of this directory.
```
$ ls
anaconda3  build  Desktop  local  packages  scratch  tmp
bin        data   dist     nb     projects  testing
```
The `ls` command provides a directory listing.
This home directory holds a set of subdirectories.

We can drill down through directories by providing arguments to `ls`.
For example, to see the contents of the **Desktop** directory, type:
```
$ ls Desktop
data-shell  data-shell.zip
```
You can see the sample files we downloaded earlier.
We can drill further; for example, to see into the directory containing
the sample files:
```
$ ls Desktop/data-shell
creatures  molecules           notes.txt  solar.pdf
data       north-pacific-gyre  pizza.cfg  writing
```


## Changing directories

Although we've peered into the directory of sample files,
we remain in the home directory.
To change directories,
use the `cd` command:
```
$ cd Desktop
$ pwd
/home/mpiper/Desktop
```
The `pwd` command shows that we've switched to the **Desktop** directory.

The `cd` command can take a directory name as an argument.
It can also take no arguments:
```
$ cd
$ pwd
/home/mpiper
```
With no arguments, `cd` always returns to your home directory.

The `cd` command can also take a set of special characters.
To switch to the previous directory,
use a dash `-`:
```
$ cd -
$ pwd
/home/mpiper/Desktop
```

When working with directories,
a dot `.` is a shortcut for the current directory,
while dot dot `..` is a shortcut for the parent directory:
```
$ cd .
$ pwd
/home/mpiper/Desktop
$ cd ..
$ pwd
/home/mpiper
```
Likewise,
the tilde `~` is a shortcut for the user's home directory:
```
$ cd ~
$ pwd
/home/mpiper
```


## Copying, moving, removing

Let's make a copy of our haiku:
```
$ cp haiku haiku-1
$ ls
haiku  haiku-1
```
The `cp` makes a duplicate of a file.

The `mv` command moves a file from one location to another.
Let's move **haiku-1** up to the **Desktop** directory:
```
$ mv haiku-1 ~/Desktop
$ ls
haiku
$ ls ~/Desktop/
shell-lesson-data  shell-lesson-data.zip  haiku-1  new
```
Note that **haiku-1** has been moved from the **new** directory to **Desktop**.

The `mv` command can also be used to rename a file.
```
$ mv ../haiku-1 haiku.copy
$ ls
haiku  haiku.copy
```
Here, we moved the file back to the **new** directory and renamed it.

Files can be deleted with the `rm` command.
Remove our haiku copy with
```
$ rm haiku.copy
$ ls
haiku
```
There is no concept of a "trash" or "recycle" bin in the shell.
Once a file is removed, it's gone, irrevocably.

As a last step,
let's move our haiku up to the parent directory,
change to the parent directory,
then delete the **new** directory:
```
$ mv haiku ..
$ cd ..
$ rmdir new
$ ls
shell-lesson-data  shell-lesson-data.zip  haiku
```
As `rm` removes files,
the `rmdir` command removes directories.
However, the directory must be empty before it can be removed.




# Making and removing directories

The filesystem is comprised of directories and files.
Here, we'll see how to make them.

To start, change to the **Desktop** directory:
```
$ cd ~/Desktop
/home/mpiper/Desktop
```
Note that by using the tilde `~`,
we'll get to the Desktop from wherever we are in the filesystem.

Next,
use the `mkdir` command to make a new directory:
```
$ mkdir new
$ ls
shell-lesson-data  shell-lesson-data.zip  new
```
Change to the new directory and get a listing:
```
$ cd new
$ ls
```
The new directory is empty.





## Summary

The table below summarizes the commands and special characters
described in this lesson.

| Command/Character | Description
| ----------------- | -----------
| pwd               | print working directory
| ls                | directory listing
| cd                | change directory
| /                 | path delimiter
| ~                 | home directory
| .                 | current directory
| ..                | one directory up
| -                 | previous directory
| cp                | copies a file
| mv                | moves or renames a file
| rm                | deletes a file (permanently)
| mkdir             | creates a directory
| rmdir             | deletes a directory (permanently)
