<img align="center" style="margin:0 0 20px 0" width="100%" height="100%" src="https://raw.githubusercontent.com/CodeToCommunicate/CoCoLessons/main/media/coco-banner.jpg">

# The terminal and shell commands

In this lesson,
we'll learn how to use one old but very effective tool,
the terminal, to execute commands on a computer.

---

## Topics | Temas

1. The terminal application and shell commands

---

1. Uso de la terminal y comandos de shell

## Goals | Objetivos

1. Open a terminal and use basic shell commands

---

1. Abrir una terminal y usar comandos básicos de shell

# Introduction to the shell | Introducción a shell

Here, we'll learn about the _shell_, a command-based interface for interacting
with the operating system of a computer.

---

Aquí, aprenderemos sobre el _shell_, que es una interfaz basada en comandos
para interactuar con el sistema operativo de una computadora.

## Open a terminal | Abrir una terminal

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

En este momento, si aún no lo has hecho, abre una terminal.

## Why are we using a terminal? | ¿Por qué usamos la terminal?

Because it works. Really well.

When you develop skill with shell commands in a terminal, you can do
filesystem-specific tasks--moving, copying, renaming, deleting files and
directories--much faster than with a graphical application.

By analogy, think of keyboard shortcuts on your computer:
if you want to change from one application to another, it's much faster to hit
`Cmd-Tab` (on macOS; `Alt-Tab` on Linux and Windows) than it is to use a mouse
to go find the other application window.

Commands tend to be terse to the point of being cryptic, not that different
from texting shorthand: instead of brb or ttyl, it's `cd` (change directory) or
`rm` (remove). And it's done for the same reason: speed.

Commands can also be gathered into _scripts_ that can be executed as a single
unit. With a script, you can automate a repetitive task.
Scripts are marvelous for data processing pipelines, and can improve
reproducibility. We won't cover scripting here, but there's more information in
Software Carpentry's
[The Unix Shell](https://swcarpentry.github.io/shell-novice/) lesson, on which
this lesson is based.

---

Porque funciona realmente bien.

Cuando utilizas los comandos de shell en una terminal, puedes realizar tareas
específicas del sistema de archivos (mover, copiar, renombrar, eliminar
archivos y directorios) mucho más rápido y eficientemente que con una
aplicación gráfica.

Por analogía, piensa en los atajos de teclado en su computadora:
si desea cambiar de una aplicación a otra, es mucho más rápido presionar
`Cmd-Tab` (en macOS; `Alt-Tab` en Linux y Windows) que usar un mouse para
buscar la ventana de la otra aplicación.

Los comandos tienden a ser concisos hasta el punto de ser crípticos, no tan
diferentes de los mensajes de texto abreviados: en lugar de tkm (te quiero
mucho) o tmb (también), es `cd` (cambiar de directorio) o `rm` (remover).
Y se hace por la misma razón: la velocidad.

Los comandos también se pueden agrupar en _scripts_ que se pueden ejecutar como
una sola unidad.
Con un script, se puede automatizar una tarea repetitiva.
Los scripts son maravillosos para construir flujos de procesamiento de datos
y pueden mejorar la reproducibilidad.
No cubriremos la creación de scripts aquí, pero hay más información en Software
Carpentry's [The Unix Shell lección](https://swcarpentry.github.io/shell-novice/),
en que se basa esta lección.

## Enter commands, get results | Ingrese comandos, obtenga resultados

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

El _prompt_ es donde ingresamos los comandos en una terminal.
Por lo general, se denota con un signo de dólar `$`.

Usamos una terminal en un
[bucle de lectura-evaluación-impresión](https://en.wikipedia.org/wiki/Read%E2%80%93eval%E2%80%93print_loop) (REPL);
esto quiere decir que cuando ingresamos un comando el interprete:

1. lee el comando
1. evalúa el comando
1. imprime salida a la terminal

Este proceso se repite cada vez que ingresamos un comando.

## Files and directories | Archivos y directorios

Information on a computer is stored in files and directories.
The part of an operating system that handles this information is called the
_filesystem_.
Think of the filesystem as a tree with branches (directories) and leaves
(files).

Let's find out where we are in the filesystem when we start a terminal:

---

La información en una computadora se almacena en archivos y directorios.
La parte del sistema operativo que maneja esta información se llama
_sistema de archivos_ (filesystem).
Piense en el sistema de archivos como un árbol con ramas (directorios) y hojas
(archivos).

Averigüemos dónde estamos en el sistema de archivos cuando iniciamos una
terminal:

```
$ pwd
/home/jupyter-mpiper
```

The `pwd` command prints the current directory to the terminal.
You can see that I'm in the directory `jupyter-mpiper` under the directory
`home`. The forward slash `/` is used as a delimiter between directory names.

This directory, `/home/jupyter-mpiper`, is special--it's the _home directory_
for the user `jupyter-mpiper`.
Every user has a home directory.
It's the default location for you to create and store information.

Note that I executed this command on a JupyterHub, which is running Linux;
the home directory on a macOS or Windows machine will be slightly different.

---

El comando `pwd` imprime en la terminal el directorio donde se encuentra
actualmente. Puedes ver que estamos en el directorio `jupyter-mpiper` debajo
del directorio `home`. La barra inclinada `/` se utiliza como delimitador entre
los nombres de los directorios.

Este directorio `/home/jupyter-mpiper` es especial. Éste es la
_carpeta de usuario_ para el usuario `jupyter-mpiper`.
Cada usuario tiene una _carpeta de usuario_ propia, que es la ubicación
predeterminada para crear y almacenar información.

Tenga en cuenta que en este caso se ejecuta este comando en JupyterHub,
que ejecuta Linux; la carpeta de usuario en una máquina macOS o Windows será
ligeramente diferente.

## Directory listings | Listados de directorios

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

El comando `ls` proporciona una lista de directorios y archivos.
La carpeta de usuario contiene un conjunto de subdirectorios.

Podemos profundizar en los directorios proporcionando argumentos a `ls`.
Por ejemplo, para ver el contenido del directorio **CoCoLessons**, escriba:

```
$ ls CoCoLessons
01_coding_environment.md       CONTRIBUTING.md
02_shell.md                    CREDITS.md
03_git_part_1.md               LICENSE
04_intro_to_python_numpy.ipynb README.md
05_matplotlib.ipynb            data
06_loops_if_functions.ipynb    environment.yml
07_pandas.ipynb                media
CODE-OF-CONDUCT.md
```

You can see the CoCo lesson files that have been added to the JupyterHub. We
can drill further; for example, to see into the directory containing data
files:

---

Puede ver los archivos de las lecciones de CoCo se agregaron a JupyterHub.
Podemos indagar más; por ejemplo, para ver el contenido del directorio llamado
`data`:

```
$ ls CoCoLessons/data RPC_4_lithologies_Messy.csv
south-africa-topography.nc.xz  temperature-central-park.dat hawaii-profile.csv
temperature-berkeley.dat       winemag-data-130k-v2.csv
```

## Changing directories | Cambiando directorios

Although we've peered into the directory of sample files, we remain in the home
directory. To change directories, use the `cd` command:

---

Aunque hemos mirado en el directorio de archivos de muestra, permanecemos en la
carpeta de usuario.
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
También se puede usar sin argumentos:

```
$ cd
$ pwd
/home/jupyter-mpiper
```

With no arguments, `cd` always returns to your home directory.

The `cd` command can also take a set of special characters as arguments.
To switch to the previous directory, use a dash `-`:

---

Sin argumentos, `cd` siempre regresa a su carpeta de usuario.

El comando `cd` también puede tomar un conjunto de caracteres especiales como
argumentos. Para cambiar al directorio anterior, use un guión `-`:

```
$ cd -
/home/jupyter-mpiper/CoCoLessons
```

When working with directories, a dot `.` is a shortcut for the current
directory, while two dots `..` are a shortcut for the parent directory:

---

Cuando se trabaja con directorios, un punto `.` es un atajo para el directorio
actual, mientras que dos puntos `..` son un atajo para el directorio-padre
(_parent directory_):

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

Asimismo, la tilde `~` es un atajo para la carpeta de usuario:

```
$ cd ~
$ pwd
/home/jupyter-mpiper
```

### Formative assessment 1

If your current directory is the **CoCoLessons** directory,
how can you get a directory listing for the **data** subdirectory?

1. `ls data`
1. `ls ./data`
1. `ls ../CoCoLessons/data`
1. `ls ~/CoCoLessons/data`
1. All of the above

Can you explain your answer?

---

Si su directorio actual es el directorio **CoCoLessons**,
¿Cómo puede obtener una lista de directorios para el subdirectorio **datos**?

1. `ls datos`
1. `ls./datos`
1. `ls ../CoCoLessons/datos`
1. `ls ~/CoCoLessons/datos`
1. Todo lo anterior

¿Puedes explicar tu respuesta?

## Making a directory | Crear un directorio

From your home directory, use the `mkdir` command to make a new directory:

---

Desde tu carpeta de usuario, usa el comando `mkdir` para crear un nuevo
directorio:

```
$ mkdir new
$ ls
CoCoLessons bin bmi-topography espin projects tmp
README.md bmi-geotiff data new scratch
```

Change to the new directory and get a listing:

---

Cambia al nuevo directorio y obtén su contenido:

```
$ cd new
$ ls
```

The new directory is empty.

---

El nuevo directorio está vacío.

## Copying, moving, and removing | Copiar, mover y eliminar

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
directorio **CoCoLessons** para obtener un archivo y copiarlo en el directorio
actual. Tenga en cuenta que la copia y el original existen y tiene el mismo
contenido:

```
$ diff -s README.md ../CoCoLessons/README.md
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

El comando `mv` también se puede usar para mover un archivo de una ubicación a
otra. Movamos **readme.md** hasta la carpeta de usuario:

```
$ mv readme.md ~
$ ls
$ ls ~
CoCoLessons bin bmi-topography espin projects scratch
README.md bmi-geotiff data new readme.md tmp
```

Note that the **new** directory is now empty because **readme.md** has been
moved up to the home directory.
Also note that **README.md** and **readme.md** in the home directory are
different files!
The filesystems in Linux and macOS are case-sensitive.

Files can be deleted with the `rm` command.
Remove our **readme.md** file with:

---

Ten en cuenta que el directorio **new** ahora está vacío porque **readme.md**
se ha movido a la carpeta de usuario.
¡También ten en cuenta que **README.md** y **readme.md** en la carpeta de
usuario son archivos diferentes!
Los sistemas de archivos en Linux y macOS distinguen entre mayúsculas y
minúsculas.

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

### Formative assessment 2

The **data** subdirectory of the **CoCoLessons** directory
contains several files.
Can you think of a way to copy all the files in a directory?

---

El subdirectorio **data** del directorio **CoCoLessons** contiene varios
archivos. ¿Puedes pensar en una manera de copiar todos los archivos en un
directorio?

## Removing a directory | Eliminar un directorio

As a last step, let's delete the **new** directory:

---

Como último paso, eliminemos el directorio **new**:

```
$ rmdir new
$ ls
CoCoLessons bin bmi-topography espin scratch
README.md bmi-geotiff data projects tmp
```

As `rm` removes files, the `rmdir` command removes directories.
However, the directory must be empty before it can be removed.

---

Como `rm` elimina archivos, el comando `rmdir` elimina directorios.
Sin embargo, el directorio debe estar vacío antes de poder eliminarlo.

### Formative assessment 3

Given that directory must be empty before it can be removed,
can you think of a way to remove all the files in a directory?
Alternately, is there a way to remove a directory even if it contains files?

---

Dado que el directorio debe estar vacío antes de poder eliminarlo,
¿Se te ocurre alguna forma de eliminar todos los archivos de un directorio?
Alternativamente, ¿hay alguna forma de eliminar un directorio incluso si
contiene archivos?

## Summary | Resumen

The table below summarizes the commands and special characters described in
this lesson.

---

La siguiente tabla resume los comandos y caracteres especiales descritos en
esta lección.

| Command/Comando | Description / Descripción                                                 |
| --------------- | ------------------------------------------------------------------------- |
| pwd             | print working directory / imprime el directorio de trabajo                |
| ls              | directory listing / muestra el contenido del directorio                   |
| cd              | change directory / cambia el directorio                                   |
| /               | path delimiter / delimitador de dirección                                 |
| ~               | home directory / carpeta de usuario                                       |
| .               | current directory / directorio actual                                     |
| ..              | one directory up / subir un directorio                                    |
| -               | previous directory / el directorio anterior                                 |
| cp              | copies a file / copia un archivo                                          |
| mv              | moves or renames a file / mueve o renombra un archivo                     |
| diff            | compares contents of files / compara el contenido de un archivo           |
| rm              | deletes a file (permanently) / elimina un archivo permanentemente         |
| mkdir           | creates a directory / crea un directorio                                  |
| rmdir           | deletes a directory (permanently) / elimina un directorio permanentemente |

## Resources | Recursos

- This lesson is loosely based on the Software Carpentry shell lesson, available in
  [English](https://swcarpentry.github.io/shell-novice/) and
  [Spanish](https://swcarpentry.github.io/shell-novice-es/)
- For a deeper dive into shell commands, see the
  [Bash Guide for Beginners](http://www.tldp.org/LDP/Bash-Beginners-Guide/html/)
  from the Linux Documentation Project, as well as the
  [GNU Bash Manual](https://www.gnu.org/software/bash/manual/)


# Homework | Tarea

After completing this lesson, please try the following:

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

- Lee la lección de shell de Software Carpentry
  ([inglés](https://swcarpentry.github.io/shell-novice/),
  [español](https://swcarpentry.github.io/shell-novice-es/))

Estas son tareas sugeridas de forma abierta: puedes hacer tanto como quieras;
no serás calificado o calificada. Lo importante es intentarlo.
Estas son herramientas que usaremos en todo CoCo,
¡así que el trabajo que haces ahora valdrá la pena más tarde!

<!-- Links, by alpha -->
```
