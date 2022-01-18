<img align="center" style="margin:0 0 20px 0" width="100%" height="100%" src="https://raw.githubusercontent.com/CodeToCommunicate/CoCoLessons/main/media/coco-banner.jpg">

# Setting up a scientific coding environment / Configurando un entorno de programación científica

In this lesson, we'll set up an environment for scientific coding that you can
use in CoCo and beyond.

## Topics

1. Project Jupyter: JupyterHub, JupyterLab, and Jupyter Notebook
1. The terminal application and shell commands

## Goals

1. Login to a JupyterHub
1. Get familiar with JupyterLab
1. Use a Jupyter Notebook
1. Open a terminal and use basic shell commands

---

En Esta lección configuraremos un entorno para realizar programación científica
que puedes usar en CoCo y para otras cosas también.

_Objetivos principales:_

1. Iniciar una sesión en JupyterHub
1. Familiarizarse con JupyterLab
1. Usar un Jupyter Notebook
1. Abrir una terminal y usar comandos básicos de shell

## Homework

After completing this lesson, please try the following:

- Create a short Jupyter Notebook that includes Python code and Markdown text,
  then run it on the JupyterHub
- Skim over the Software Carpentry shell lesson
  ([English](https://swcarpentry.github.io/shell-novice/),
  [Spanish](https://swcarpentry.github.io/shell-novice-es/))

These are open-ended assignments: you can do as much or as little as you'd like,
you will not be graded.
The important thing is to try them;
they're tools that we'll be using throughout CoCo, so the work you put in now
will pay off later!

---

Después de completar esta lección, realiza las siguiente tareas:

- Crea un Jupyter Notebook corto que incluya código Python y texto Markdown,
  luego ejecútalo en JupyterHub
- Lea la lección de shell de Software Carpentry
  ([inglés](https://swcarpentry.github.io/shell-novice/),
  [español](https://swcarpentry.github.io/shell-novice-es/) )

Estas son asignaciones abiertas: puede hacer tanto o tan poco como quieras;
no serás calificado. Lo importante es probarlos.
Estas son herramientas que usaremos en todo CoCo,
¡así que el trabajo que haces ahora valdrá la pena más tarde!

# Project Jupyter / Proyecto Jupyter

<img align="right" width="150" height="150" src="https://jupyter.org/assets/homepage/main-logo.svg">

[Project Jupyter][jupyter] is a non-profit, open-source, community-driven
organization that oversees the development of a software ecosystem for
interactive scientific coding, learning, and discovery.
Project Jupyter grew out of the [IPython project][ipython] started by Fernando
P&eacute;rez when we was a graduate student in physics at the University of
Colorado Boulder.

In CoCo, we'll use three tools from the Project Jupyter ecosystem:
JupyterHub, JupyterLab, and Jupyter Notebook.

---

[Project Jupyter][jupyter] es una organización sin fines de lucro, de código
abierto e impulsada por la comunidad que supervisa el desarrollo de un
ecosistema de software para programación científica interactiva, el aprendizaje
y el descubrimiento.
El proyecto Jupyter surgió del [proyecto IPython][ipython] iniciado por Fernando
Pérez cuando éramos estudiantes de posgrado en física en la Universidad de
Colorado Boulder.

En Coco, usaremos tres herramientas del ecosistema proyecto Jupyter:
JupyterHub, JupyterLab y Jupyter Notebook.

## JupyterHub

A [JupyterHub](https://jupyter.org/hub) is a server system that allows multiple
users access to a computational resource, where each user can run Jupyter
Notebook and other software in their own workspace.
A JupyterHub can be installed in the cloud or locally.

Through the NSF-funded [OpenEarthscape][oes] project,
the [Community Surface Dynamics Modeling System][csdms] (CSDMS)
provides a [JupyterHub][csdms-jhub] where CoCo notebooks can be run.
Click this button [![Run on CSDMS JupyterHub][badge]][csdms-jhub-link]
to open the CoCo lessons directly on the CSDMS JupyterHub!

---

[JupyterHub](https://jupyter.org/hub) es un sistema de servidor que permite que
múltiples usuarios accedan a un recurso computacionales, donde cada usuario
puede ejecutar Jupyter Notebook y otro software en su propio espacio de trabajo.
Un JupyterHub se puede instalar en la nube o localmente.

A través del proyecto [OpenEarthscape][oes] financiado por la NSF,
el [Community Surface Dynamics Modeling System][csdms] (CSDMS) proporciona un
[JupyterHub][csdms-jhub] donde se pueden ejecutar los portátiles del programa CoCo.
Haga clic en este botón [![Ejecutar en CSDMS JupyterHub][badge]][csdms-jhub-link]
para abrir las lecciones de CoCo directamente en CSDMS JupyterHub.

## JupyterLab

JupyterLab is a browser-based interactive development environment.
It provides tools for writing code and creating notebooks, including

- a file browser,
- launchers for notebooks, data files, and images,
- terminal, text editor, and code console applications, and
- keyboard shortcuts to speed your work.

JupyterLab is the default user interface for JupyterHub.
Like JupyterHub, JupyterLab can be installed in the cloud or locally.

---

JupyterLab es un entorno de desarrollo interactivo basado para el navegador.
Proporciona herramientas para escribir código y crear notebooks, como también:

- un explorador de archivos,
- lanzadores para notebooks, archivos de datos e imágenes,
- aplicaciones de terminal, editor de texto y consola/terminales de código, y
- atajos de teclado para acelerar su trabajo.

JupyterLab es la interfaz de usuario predeterminada para JupyterHub.
Al igual que JupyterHub, JupyterLab se puede instalar en la nube o localmente.

## Jupyter Notebook

A Jupyter Notebook is an interactive document for writing, explaining, and
running code, and for communicating results.

Notebooks are live documents, with the ability to display graphics and tabular data,
as well as interactive displays with widgets.
A notebook is made of cells.
Each cell can hold code, text (using Markdown), equations, or visualizations.

To get a sense of their popularity,
by [one estimate](https://github.com/parente/nbestimate/blob/master/estimate.ipynb),
there are currently over 7.5 million notebooks currently hosted on GitHub.
The estimate is presented, of course, in a notebook.

---

Jupyter Notebook es un documento interactivo para escribir, explicar y ejecutar
código, y para comunicar resultados.

Los notebooks son documentos dinámicos, con la capacidad de mostrar gráficos y
datos tabulares, así como pantallas interactivas con widgets.
Un notebook está hecho de celdas.
Cada celda puede contener código, texto (usando Markdown), ecuaciones o
visualizaciones.

Para tener una idea de su popularidad,
[se estima](https://github.com/parente/nbestimate/blob/master/estimate.ipynb)
que actualmente hay más de 7,5 millones de notebooks alojados en GitHub.
La estimación se presenta, por supuesto, en un notebook.

## Resources /Recursos

- [Project Jupyter][jupyter]
- JupyterHub [documentation][jupyterhub-docs]
- JupyterLab [documentation][jupyterlab-docs] and
  [an entertaining demonstration](https://youtu.be/A5YyoCKxEOU) on YouTube
- Jupyter Notebook [documentation][jupyter-notebook-docs]
- The [first section][swc-ppp-1] of the Software Carpentry
  [Plotting and Programming in Python][swc-ppp] lesson has a great section on
  JupyterLab and Jupyter Notebook
- A collection of [notable Jupyter Notebooks](https://github.com/jupyter/jupyter/wiki)
  and a comprehensive [tutorial](https://www.dataquest.io/blog/jupyter-notebook-tutorial/)

# Introduction to the shell / Introducción a shell

Here, we'll learn about the _shell_, a command-based interface for interacting
with the operating system of a computer.

---

Aquí, aprenderemos sobre el _shell_, que es una interfaz basada en comandos para
interactuar con el sistema operativo de una computadora.

## Open a terminal / Abrir una terminal

A _terminal_ is an application that allows a user to communicate with the
operating system of a computer through terse text commands.

- JupyterLab: Terminal app in the Launcher
- Linux: terminal or xterm
- macOS: Terminal.app (built-in) or [iTerm.app](https://www.iterm2.com/) (better)
- Windows: Git Bash Shell in [Git for Windows](https://gitforwindows.org/)

At this time, if you haven't already done so, open a terminal.

---

Una _terminal_ es una aplicación que permite a un usuario comunicarse con el
sistema operativo de una computadora a través de comandos de texto concisos.

- JupyterLab: tiene una aplicación de terminal en el lanzador
- Linux: terminal o xterm
- macOS: Terminal.app (integrado) o [iTerm.app](https://www.iterm2.com/) (mejor)
- Windows: Git Bash Shell en [Git para Windows](https://gitforwindows.org/)

En este momento, si aún no lo ha hecho, abra una terminal.

## Why are we using a terminal? / ¿Por qué usamos la terminal?

Because it works. Really well.

When you develop skill with shell commands in a terminal, you can do
filesystem-specific tasks--moving, copying, renaming, deleting files and
directories--much faster than with a graphical application.

By analogy, think of keyboard shortcuts on your computer:
if you want to change from one application to another, it's much faster to hit
`Cmd-Tab` (on macOS; `Alt-Tab` on Linux and Windows) than it is to use a mouse
to go find the other application window.

Commands tend to be terse to the point of being cryptic, not that different
from texting shorthand: instead of brb or ttyl, it's `cd` or `rm`.
And it's done for the same reason: speed.

Commands can also be gathered into _scripts_ that can be executed as a single unit.
With a script, you can automate a repetitive task.
Scripts are marvelous for data processing pipelines, and can improve reproducibility.
We won't cover scripting here, but there's more information in Software Carpentry's
[The Unix Shell](https://swcarpentry.github.io/shell-novice/) lesson, on which
this lesson is based.

---

Porque funciona realmente bien.

Cuando utiliza los comandos de shell en una terminal, puede realizar tareas
específicas del sistema de archivos (mover, copiar, renombrar, eliminar archivos
y directorios) mucho más rápido y eficientemente que con una aplicación gráfica.

Por analogía, piense en los atajos de teclado en su computadora:
si desea cambiar de una aplicación a otra, es mucho más rápido presionar
`Cmd-Tab` (en macOS; `Alt-Tab` en Linux y Windows) que usar un mouse para buscar
la ventana de la otra aplicación.

Los comandos tienden a ser concisos hasta el punto de ser crípticos, no tan
diferentes de los mensajes de texto abreviados: en lugar de tkm (te quiero mucho)
o tmb (también), es `cd` o `rm`.
Y se hace por la misma razón: la velocidad.

Los comandos también se pueden agrupar en _scripts_ que se pueden ejecutar como
una sola unidad.
Con un script, puede automatizar una tarea repetitiva.
Los scripts son maravillosos para las canalizaciones de procesamiento de datos
y pueden mejorar la reproducibilidad.
No cubriremos la creación de scripts aquí, pero hay más información en Software
Carpentry's [The Unix Shell lección](https://swcarpentry.github.io/shell-novice/),
en que se basa esta lección.

## Enter commands, get results / Ingrese comandos, obtenga resultados

The command prompt (or shell prompt) is where we enter commands into a terminal.
It's typically denoted with a dollar sign `$`.

We use a terminal in a
[read-evaluate-print loop](https://en.wikipedia.org/wiki/Read%E2%80%93eval%E2%80%93print_loop) (REPL);
that is, when we enter a command at the prompt, the shell:

1. reads the command
1. evaluates the command
1. prints output to the terminal

This process is repeated every time we enter a command.

---

El prompt del sistema es donde ingresamos los comandos en una terminal.
Por lo general, se denota con un signo de dólar `$`.

Usamos una terminal en un
[bucle de lectura-evaluación-impresión](https://en.wikipedia.org/wiki/Read%E2%80%93eval%E2%80%93print_loop) (REPL);
esto quiere decir que cuando ingresamos un comando el interprete:

1. lee el comando
1. evalúa el comando
1. imprime salida a la terminal

Este proceso se repite cada vez que ingresamos un comando.

## Files and directories / Archivos y directorios

Information on a computer is stored in files and directories.
The part of an operating system that handles this information is called the
_filesystem_.
Think of the filesystem as a tree with branches (directories) and leaves (files).

Let's find out where we are in the filesystem when we start a terminal:

---

La información en una computadora se almacena en archivos y directorios.
La parte del sistema operativo que maneja esta información se llama
_sistema de archivos_ (filesystem).
Piense en el sistema de archivos como un árbol con ramas (directorios) y hojas (archivos).

Averigüemos dónde estamos en el sistema de archivos cuando iniciamos una terminal:

```
$ pwd
/home/jupyter-mpiper
```

The `pwd` command prints the current directory to the terminal.
You can see that I'm in the directory `jupyter-mpiper` under the directory `home`.
The forward slash `/` is used as a delimiter between directory names.

This directory, `/home/jupyter-mpiper`, is special--it's the _home directory_
for the user `jupyter-mpiper`.
Every user has a home directory.
It's the default location for you to create and store information.

Note that I executed this command on a JupyterHub, which is running Linux;
the home directory on a macOS or Windows machine will be slightly different.

---

El comando `pwd` imprime en la terminal el directorio donde se encuentra actualmente.
Puedes ver que estamos en el directorio `jupyter-mpiper` debajo del directorio `home`.
La barra inclinada `/` se utiliza como delimitador entre los nombres de los directorios.

Este directorio `/home/jupyter-mpiper` es especial. Éste es el
_directorio de inicio_ para el usuario `jupyter-mpiper`.
Cada usuario tiene un directorio de inicio, que es la ubicación predeterminada
para crear y almacenar información.

Tenga en cuenta que en este caso se ejecuta este comando en JupyterHub,
que ejecuta Linux; el directorio de inicio en una máquina macOS o Windows será
ligeramente diferente.

## Directory listings / Listados de directorios

Next, let's look at the contents of this directory:

---

A continuación, veamos el contenido de este directorio:

```
$ ls
CoCoLessons  bin          bmi-topography  espin     scratch
README.md    bmi-geotiff  data            projects  tmp
```

The `ls` command provides a directory listing.
This home directory holds a set of subdirectories.

We can drill down through directories by providing arguments to `ls`.
For example, to see the contents of the **CoCoLessons** directory, type:

---

El comando `ls` proporciona una lista de directorios.
Este directorio de inicio contiene un conjunto de subdirectorios.

Podemos profundizar en los directorios proporcionando argumentos a `ls`.
Por ejemplo, para ver el contenido del directorio **CoCoLessons**, escriba:

```
$ ls CoCoLessons
data                          coco_3_matplotlib.ipynb          CONTRIBUTING.md   README.md
media                         coco_4_functions_and_more.ipynb  CREDITS.md
coco_1_coding_environment.md  coco_5_pandas.ipynb              environment.yaml
coco_2_python_basics.ipynb    CODE-OF-CONDUCT.md               LICENSE.md
```

You can see the CoCo lesson files that have been added to the JupyterHub.
We can drill further; for example, to see into the directory containing data files:

---

Puede ver los archivos de las lecciones de CoCo se agregaron a JupyterHub.
Podemos indagar más; por ejemplo, para ver el contenido del directorio llamado data:

```
$ ls CoCoLessons/data
RPC_4_lithologies_Messy.csv  south-africa-topography.nc.xz  temperature-central-park.dat
hawaii-profile.csv           temperature-berkeley.dat       winemag-data-130k-v2.csv
```

## Changing directories / Cambiando directorios

Although we've peered into the directory of sample files, we remain in the home directory.
To change directories, use the `cd` command:

---

Aunque hemos mirado en el directorio de archivos de muestra, permanecemos en el
directorio de inicio.
Para cambiar de directorio, use el comando `cd`:

```
$ cd CoCoLessons
$ pwd
/home/jupyter-mpiper/CoCoLessons
```

The `pwd` command shows that we've switched to the **CoCoLessons** directory.

The `cd` command can take a directory name as an argument.
It can also take no arguments:

---

El comando `pwd` muestra que hemos cambiado al directorio **CoCoLessons**.

El comando `cd` puede tomar un nombre de directorio como argumento.
También puede tomar sin argumentos:

```
$ cd
$ pwd
/home/jupyter-mpiper
```

With no arguments, `cd` always returns to your home directory.

The `cd` command can also take a set of special characters as arguments.
To switch to the previous directory, use a dash `-`:

---

Sin argumentos, `cd` siempre regresa a su directorio de inicio.

El comando `cd` también puede tomar un conjunto de caracteres especiales como argumentos.
Para cambiar al directorio anterior, use un guión `-`:

```
$ cd -
/home/jupyter-mpiper/CoCoLessons
```

When working with directories, a dot `.` is a shortcut for the current directory,
while two dots `..` are a shortcut for the parent directory:

---

Cuando se trabaja con directorios, un punto `.` es un atajo para el directorio
actual, mientras que dos puntos `..` son un atajo para el directorio principal:

```
$ cd .
$ pwd
/home/jupyter-mpiper/CoCoLessons
$ cd ..
$ pwd
/home/jupyter-mpiper
```

Likewise, the tilde `~` is a shortcut for the user's home directory:

---

Asimismo, la tilde `~` es un atajo para el directorio de inicio del usuario:

```
$ cd ~
$ pwd
/home/jupyter-mpiper
```

## Making a directory

From your home directory, use the `mkdir` command to make a new directory:

---

Desde su directorio de inicio, use el comando `mkdir` para crear un nuevo directorio:

```
$ mkdir new
$ ls
CoCoLessons  bin          bmi-topography  espin  projects  tmp
README.md    bmi-geotiff  data            new    scratch
```

Change to the new directory and get a listing:

---

Cambie al nuevo directorio y obtenga su contenido:

```
$ cd new
$ ls
```

The new directory is empty.

---

El nuevo directorio está vacío.

## Copying, moving, and removing / Copiar, mover y eliminar

Let's copy a file from the **CoCoLessons** directory to our **new** directory:

---

Copiemos un archivo del directorio **CoCoLessons** a nuestro **new** directorio:

```
$ cp ../CoCoLessons/README.md .
$ ls
README.md
```

Here, we instructed the `cp` command to go up a directory and over to the
**CoCoLessons** directory to get a file and copy it to the current directory.
Note that the copy and the original both exist, and are the same:

---

Aquí, le indicamos al comando `cp` que subiera un directorio y fuera al
directorio **CoCoLessons** para obtener un archivo y copiarlo en el directorio actual.
Tenga en cuenta que la copia y el original existen y son los mismos:

```
$ $ diff -s README.md ../CoCoLessons/README.md
Files README.md and ../CoCoLessons/README.md are identical
```

The `diff` command compares files and reports how they differ.

The `mv` command can be used to rename a file.

---

El comando `diff` compara archivos e informa en qué se diferencian.

El comando `mv` se puede utilizar para cambiar el nombre de un archivo.

```
$ mv README.md readme.md
$ ls
readme.md
```

The `mv` command can also be used to move a file from one location to another.
Let's move **readme.md** up to the home directory:

---

El comando `mv` también se puede usar para mover un archivo de una ubicación a otra.
Movamos **readme.md** hasta el directorio de inicio:

```
$ mv readme.md ~
$ ls
$ ls ~
CoCoLessons  bin          bmi-topography  espin  projects   scratch
README.md    bmi-geotiff  data            new    readme.md  tmp
```

Note that the **new** directory is now empty because **readme.md** has been
moved up to the home directory.
Also note that **README.md** and **readme.md** in the home directory are
different files!
The filesystems in Linux and macOS are case-sensitive.

Files can be deleted with the `rm` command.
Remove our **readme.md** file with:

---

Tenga en cuenta que el directorio **new** ahora está vacío porque **readme.md**
se ha movido al directorio de inicio.
¡También tenga en cuenta que **README.md** y **readme.md** en el directorio de
inicio son archivos diferentes!
Los sistemas de archivos en Linux y macOS distinguen entre mayúsculas y minúsculas.

Los archivos se pueden eliminar con el comando `rm`.
Elimina nuestro archivo **readme.md** con:

```
$ cd
$ rm readme.md
```

There is no concept of a "trash" or "recycle" bin in the shell.
Once a file is removed, it's gone, irrevocably.

---

No existe el concepto de "papelera" o "papelera de reciclaje" en el shell.
Una vez que se elimina un archivo, desaparece irrevocablemente.

## Removing a directory / Eliminar un directorio

As a last step, let's delete the **new** directory:

---

Como último paso, eliminemos el directorio **new**:

```
$ rmdir new
$ ls
CoCoLessons  bin          bmi-topography  espin     scratch
README.md    bmi-geotiff  data            projects  tmp
```

As `rm` removes files, the `rmdir` command removes directories.
However, the directory must be empty before it can be removed.

---

Como `rm` elimina archivos, el comando `rmdir` elimina directorios.
Sin embargo, el directorio debe estar vacío antes de poder eliminarlo.

## Summary / Resumen

The table below summarizes the commands and special characters described in this lesson.

---

La siguiente tabla resume los comandos y caracteres especiales descritos en esta lección.

| Command/Comando | Description / Descripción                                                 |
| --------------- | ------------------------------------------------------------------------- |
| pwd             | print working directory / imprime el directorio de trabajo                |
| ls              | directory listing / muestra el contenido del directorio                   |
| cd              | change directory / cambia el directorio                                   |
| /               | path delimiter / delimitador de dirección                                 |
| ~               | home directory / directorio de inicio                                     |
| .               | current directory / directorio actual                                     |
| ..              | one directory up / subir un directorio                                    |
| -               | previous directory / un directorio arriba                                 |
| cp              | copies a file / copia un archivo                                          |
| mv              | moves or renames a file / mueve o renombra un archivo                     |
| diff            | compares contents of files / compara el contenido de un archivo           |
| rm              | deletes a file (permanently) / elimina un archivo permanentemente         |
| mkdir           | creates a directory / crea un directorio                                  |
| rmdir           | deletes a directory (permanently) / elimina un directorio permanentemente |

## Resources / Recursos

- This lesson is loosely based on the Software Carpentry shell lesson, available in
  [English](https://swcarpentry.github.io/shell-novice/) and
  [Spanish](https://swcarpentry.github.io/shell-novice-es/)
- For a deeper dive into shell commands, see the
  [Bash Guide for Beginners](http://www.tldp.org/LDP/Bash-Beginners-Guide/html/)
  from the Linux Documentation Project, as well as the
  [GNU Bash Manual](https://www.gnu.org/software/bash/manual/)

<!-- Links, by alpha -->

[badge]: https://img.shields.io/badge/CSDMS-JupyterHub-orange.svg
[csdms]: https://csdms.colorado.edu
[csdms-jhub]: https://lab.openearthscape.org
[csdms-jhub-link]: https://lab.openearthscape.org/hub/user-redirect/git-pull?repo=https%3A%2F%2Fgithub.com%2FCodeToCommunicate%2FCoCoLessons&urlpath=lab%2Ftree%2FCoCoLessons%2F%3Fautodecode&branch=main
[ipython]: https://ipython.org/
[jupyter]: https://jupyter.org/
[jupyterhub-docs]: (https://jupyterhub.readthedocs.io)
[jupyterlab-docs]: (https://jupyterlab.readthedocs.io)
[jupyter-notebook-docs]: https://jupyter-notebook.readthedocs.io
[oes]: https://openearthscape.org/
[swc-ppp]: https://swcarpentry.github.io/python-novice-gapminder/
[swc-ppp-1]: https://swcarpentry.github.io/python-novice-gapminder/01-run-quit/index.html
