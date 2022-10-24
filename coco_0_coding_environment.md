<img align="center" style="margin:0 0 20px 0" width="100%" height="100%" src="https://raw.githubusercontent.com/CodeToCommunicate/CoCoLessons/main/media/coco-banner.jpg">

# Setting up a scientific coding environment / Configurando un entorno de programación científica

In this lesson, we'll set up an environment for scientific coding that you can
use in CoCo and beyond.

---

En Esta lección configuraremos un entorno para realizar programación científica
que puedes usar en CoCo y para otras cosas también.

## Topics

1. Python distribution
1. Terminal application
1. Text editor

---

1. 
1. 
1. 

## Goals / Objetivos

1. Install Anaconda Distribution
1. Locate a terminal application (Linux or macOS), or install Git for Windows (Windows)
1. Install VS Code

---

1. 
1. 
1. 

# A scientific coding environment

We will install three pieces of software--a Python distribution,
a terminal application, and a text editor--that together
form a basic scientific coding environment.

## Python distribution

The most important application we will need for our scientific coding
environment is a *Python distribution*.

Most computers already have a Python distribution installed
with the operating system (OS).
However, it's best not to work with this distribution
because changes to it may break things on your computer.

<!-- Todo: update image URL -->

<img align="right" style="margin:10px 0 10px 10px" width="20%" src="./media/logo-full-green-anaconda.png">

Instead,
we recommend installing a scientific Python distribution.
One popular example is the [Anaconda Distribution][anaconda-distribution].
It includes a standard Python distribution,
a number of important scientific libraries,
and a package manager, `conda`.

The Anaconda Distribution is available for Linux, macOS, and Windows.
Please follow the link below to download, then install, the Anaconda Distribution on your computer.

https://www.anaconda.com/products/distributino

## Terminal application

The second application we need for our scientific coding environment
is a *terminal*, also referred to as a *command line* or a *shell*.
Terminals allow you interact with a computer's OS through a command language.
Terminals are old technology,
but they're still popular and widely used because they're so efficient.

Depending on the OS of your computer,
you may have to download and install a terminal application,
or one may be installed already.

### Windows

<!-- Todo: update image URL -->

<img align="right" style="margin:10px 0 10px 10px" width="20%" src="./media/git_logo.png">

If your computer is running Windows,
you'll need to install a terminal application.
There are a few options to do so;
we currently recommend [Git for Windows][git-for-windows].
Not only does it emulate a terminal on Windows,
but it includes Git software,
which we'll learn about and use later.

Please follow the link below to download, then install, Git for Windows on your computer.

https://gitforwindows.org/

<!-- Todo: Note install instructions--include in path. -->

Once installed,
you can run the program Git Bash from the Start menu.

### Linux and macOS

If your computer is running Linux or macOS,
a terminal application is already installed by default.

* macOS: Open Finder, then select *Applications > Utilities > Terminal.app*
* Linux: It depends on the distribution, but you can find the terminal application in the applications menu

## Text editor

The final application we need to complete our scientific coding environment
is a *text editor*.

<!-- Todo: update image URL -->

<img align="right" style="margin:10px 0 10px 10px" width="20%" src="./media/Visual_Studio_Code_1.35_icon.svg.png">

https://code.visualstudio.com/

# Summary

The software we've installed---a Python distribution, a terminal application, and a text editor---form the basis of a scientific coding environment.

We will do more work to configure this scientific coding environment as we progress through CoCo.

By the end of CoCo,
you will be able to use these tools in your research,
and they'll live on your computer long after CoCo.

<!-- Links, by alpha -->
[anaconda-distribution]: https://www.anaconda.com/products/distribution
[git-for-windows]: https://gitforwindows.org/
