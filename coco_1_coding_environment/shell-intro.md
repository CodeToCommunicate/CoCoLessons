![CoCo logo](./media/coco-banner.jpg)

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

We use a terminal in a [read-evaluate-print loop](https://en.wikipedia.org/wiki/Read%E2%80%93eval%E2%80%93print_loop) (REPL);
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
CoCoLessons  bin          bmi-topography  espin     scratch
README.md    bmi-geotiff  data            projects  tmp
```
The `ls` command provides a directory listing.
This home directory holds a set of subdirectories.

We can drill down through directories by providing arguments to `ls`.
For example, to see the contents of the **CoCoLessons** directory, type:
```
$ ls CoCoLessons
CODE-OF-CONDUCT.md  Coco_Session2.ipynb  LICENSE.md                 environment.yaml
CONTRIBUTING.md     Coco_Session3.ipynb  README.md                  media
CREDITS.md          Coco_Session4.ipynb  coco_1_coding_environment
Coco_Session1.pptx  Coco_Session5.ipynb  data
```
You can see the CoCo lesson files that have been added to the JupyterHub.
We can drill further; for example, to see into the directory containing
data files:
```
$ ls CoCoLessons/data
RPC_4_lithologies_Messy.csv  south-africa-topography.nc.xz  temperature-central-park.dat
hawaii-profile.csv           temperature-berkeley.dat       winemag-data-130k-v2.csv
```


## Changing directories

Although we've peered into the directory of sample files,
we remain in the home directory.
To change directories,
use the `cd` command:
```
$ cd CoCoLessons
$ pwd
/home/jupyter-mpiper/CoCoLessons
```
The `pwd` command shows that we've switched to the **CoCoLessons** directory.

The `cd` command can take a directory name as an argument.
It can also take no arguments:
```
$ cd
$ pwd
/home/jupyter-mpiper
```
With no arguments, `cd` always returns to your home directory.

The `cd` command can also take a set of special characters as arguments.
To switch to the previous directory,
use a dash `-`:
```
$ cd -
/home/jupyter-mpiper/CoCoLessons
```

When working with directories,
a dot `.` is a shortcut for the current directory,
while two dots `..` are a shortcut for the parent directory:
```
$ cd .
$ pwd
/home/jupyter-mpiper/CoCoLessons
$ cd ..
$ pwd
/home/jupyter-mpiper
```
Likewise,
the tilde `~` is a shortcut for the user's home directory:
```
$ cd ~
$ pwd
/home/jupyter-mpiper
```

## Making a directory

From your home directory,
use the `mkdir` command to make a new directory:
```
$ mkdir new
$ ls
CoCoLessons  bin          bmi-topography  espin  projects  tmp
README.md    bmi-geotiff  data            new    scratch
```
Change to the new directory and get a listing:
```
$ cd new
$ ls
```
The new directory is empty.


## Copying, moving, and removing

Let's copy a file from the **CoCoLessons** directory to our **new** directory:
```
$ cp ../CoCoLessons/README.md .
$ ls
README.md
```
Here, we instructed the `cp` command to go up a directory
and over to the **CoCoLessons** directory to get a file and copy it to the current directory.
Note that the copy and the original both exist, and are the same:
```
$ $ diff -s README.md ../CoCoLessons/README.md
Files README.md and ../CoCoLessons/README.md are identical
```
The `diff` command compares files and reports how they differ.


The `mv` command can be used to rename a file.
```
$ mv README.md readme.md
$ ls
readme.md
```
The `mv` command can also be used to move a file from one location to another.
Let's move **readme.md** up to the home directory:
```
$ mv readme.md ~
$ ls
$ ls ~
CoCoLessons  bin          bmi-topography  espin  projects   scratch
README.md    bmi-geotiff  data            new    readme.md  tmp
```
Note that the **new** directory is now empty because **readme.md** has been moved up to the home directory.
Also note that **README.md** and **readme.md** in the home directory are different files!
The filesystems in Linux and macOS are case-sensitive.

Files can be deleted with the `rm` command.
Remove our **readme.md** file with
```
$ cd
$ rm readme.md
```
There is no concept of a "trash" or "recycle" bin in the shell.
Once a file is removed, it's gone, irrevocably.


## Removing a directory

As a last step,
let's delete the **new** directory:
```
$ rmdir new
$ ls
CoCoLessons  bin          bmi-topography  espin     scratch
README.md    bmi-geotiff  data            projects  tmp
```
As `rm` removes files,
the `rmdir` command removes directories.
However, the directory must be empty before it can be removed.


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
| diff              | compares contents of files
| rm                | deletes a file (permanently)
| mkdir             | creates a directory
| rmdir             | deletes a directory (permanently)


## Resources

* This lesson is loosely based on the Software Carpentry shell lesson, available in [English](https://swcarpentry.github.io/shell-novice/) and [Spanish](https://swcarpentry.github.io/shell-novice-es/)
* For a deeper dive into shell commands, see the [Bash Guide for Beginners](http://www.tldp.org/LDP/Bash-Beginners-Guide/html/) from the Linux Documentation Project, as well as the [GNU Bash Manual](https://www.gnu.org/software/bash/manual/)

___

[Setting up a scientific coding environment](./index.md) |
Previous: [Project Jupyter](./jupyter.md)
