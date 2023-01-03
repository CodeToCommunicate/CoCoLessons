<a href="https://www.codecommunicate.org/">
    <img align="center" style="margin:0 0 20px 0" width="100%" height="100%"
    src="https://raw.githubusercontent.com/CodeToCommunicate/CoCoLessons/main/media/coco-banner.jpg">
    </a>

# Setting up a scientific coding environment | Configurando un entorno de programación científica

In this lesson, we'll set up an environment for scientific coding that you can
use in CoCo and beyond.
We'll also learn about Project Jupyter and the tools it provides for scientific coding.

---

En esta lección configuraremos un entorno para realizar programación científica
que puedes usar en CoCo y para otras cosas también.

## Topics | Temas

1. Python distribution
1. Terminal application
1. Text editor
1. Project Jupyter: JupyterHub, JupyterLab, and Jupyter Notebook

---

1. Distribuciones de Python
1. Terminal
1. Editor de texto
1. Proyecto Jupyter: JupyterHub, JupyterLab y Jupyter Notebook

## Goals | Objetivos

1. Install Anaconda Distribution
1. Locate a terminal application (Linux or macOS), or install Git for Windows
   (Windows)
1. Install VS Code
1. Login to a JupyterHub
1. Get familiar with JupyterLab
1. Use a Jupyter Notebook

---

1. Instalar la distribución Anaconda
1. Localizar la terminal (en Linux o macOS) o istalar Git para Windows
   (Wisndows)
1. Instalar VS Code
1. Iniciar una sesión en JupyterHub
1. Familiarizarse con JupyterLab
1. Usar un Jupyter Notebook

# A scientific coding environment | Entorno para programación científica

We will install three pieces of software: a Python distribution, a terminal
application, and a text editor--that together form a basic scientific coding
environment.

---

Instalaremos tres piezas de software: una distribución de Python, una
aplicación de terminal y un editor de texto. Todo junto forman un entorno de
programación científica básica.

## Python distribution | Distribución de Python

The first application we need for our scientific coding environment is a
_Python distribution_, the set of tools and libraries for developing code in
Python.

Most computers already have a Python distribution installed with the operating
system (OS). However, it's best not to work with this distribution because
changes to it may break things on your computer.

<!-- Todo: update image src URL -->

<a href="https://www.anaconda.com/products/distribution">
    <img align="right" style="margin:10px 0 10px 10px" width="20%"
    src="./media/logo-full-green-anaconda.png"> </a>

Instead, we recommend installing a scientific Python distribution.
One popular example is the [Anaconda Distribution][anaconda-distribution].
It includes a standard Python distribution, a number of important scientific
libraries, and a package manager, `conda`.

The Anaconda Distribution is available for Linux, macOS, and Windows.
Please click the Anaconda logo on the right (or use the link above) to
download, then install, the Anaconda Distribution on your computer.

The Anaconda Distribution comes with many tools for working with Python.
We'll explore some of these as we progress through CoCo.

---

La primera aplicación que necesitamos para nuestro entorno de programación
científica es una distribución de Python, el conjunto de herramientas y
librerías para desarrollar código en Python.

La mayoría de las computadoras ya tienen instalada una distribución de Python
con el sistema operativo (SO).
Sin embargo, es mejor no trabajar con esta distribución porque los cambios en
ella pueden dañar las cosas en su computadora.

En su lugar, recomendamos instalar una distribución científica de Python.
Un ejemplo popular es la Distribución Anaconda.
Incluye una distribución estándar de Python, varias librerías científicas
importantes y un administrador de paquetes, conda.

La distribución de Anaconda está disponible para Linux, macOS y Windows.
Haga clic en el logotipo de Anaconda a la derecha (o use el enlace de arriba)
para descargar e instalar Anaconda Distribution en su computadora.

La distribución Anaconda viene con muchas herramientas para trabajar con Python.
Exploraremos algunos de estos a medida que avanzamos en CoCo.

## Terminal application | Terminal

The second application we need for our scientific coding environment is a
_terminal_, also referred to as a _command line_ or a _shell_. Terminals allow
you interact with a computer's OS through a command language.
Terminals are old technology, but they're still popular and widely used because
they're so efficient.

Depending on the OS of your computer, you may have to download and install a
terminal application, or one may be installed already.

---

La segunda aplicación que necesitamos para nuestro entorno de programación
científica es una terminal, también conocida como _línea de comandos_ o
_shell_.
Los terminales permiten interactuar con el sistema operativo de una
computadora a través de un lenguaje de comandos.
Los terminales son tecnología antigua, pero siguen siendo populares y
ampliamente utilizados porque son muy eficientes.

Según el sistema operativo de su computadora, es posible que deba descargar e
instalar una aplicación de terminal, o es posible que ya haya una instalada.

### Windows

<!-- Todo: update image URL -->

<a href="https://gitforwindows.org/">
    <img align="right" style="margin:10px 0 10px 10px" width="20%"
    src="./media/git_logo.png">
</a>

If your computer is running Windows, you'll need to install a terminal
application. There are a few options to do so; we currently recommend
[Git for Windows][git-for-windows].
Not only does it emulate a terminal on Windows, but it also includes Git
software, which we'll learn about and use later.

Please click the logo on the right (or use the link above) to download Git for
Windows to your computer.

When installing Git for Windows, please carefully follow the
[instructions][git-install-instructions] provided by Software Carpentry.
This will ensure Git and Anaconda work together correctly.

Once installed, you can run the program Git Bash from the Start menu.

---

Si su computadora ejecuta Windows, deberá instalar una aplicación de terminal.
Hay algunas opciones para hacerlo; actualmente recomendamos
[Git para Windows][git-for-windows].
No solo emula una terminal en Windows, sino que también incluye el software
Git, que aprenderemos y usaremos más adelante.

Haga clic en el logotipo a la derecha (o use el enlace de arriba) para
descargar Git para Windows en su computadora.

Al instalar Git para Windows, siga cuidadosamente las
[instrucciones][git-install-instructions] proporcionadas por Software
Carpentry.
Esto asegurará que Git y Anaconda funcionen juntos correctamente.

Una vez instalado, puede ejecutar el programa Git Bash desde el menú Inicio.

### Linux and macOS

If your computer is running Linux or macOS, a terminal application is already
installed by default.

- macOS: Open Finder, then select _Applications > Utilities > Terminal.app_
- Linux: It depends on the distribution, but you can find the terminal
  application in the applications menu

---

Si su computadora ejecuta Linux o macOS, una aplicación de terminal ya está
instalada de manera predeterminada.

- macOS: Abra Finder, luego seleccione _Aplicaciones > Utilidades > Terminal.app_
- Linux: Depende de la distribución, pero puedes encontrar la aplicación de
  terminal en el menú de aplicaciones

## Text editor | Editor de texto

The final application we need to complete our scientific coding environment
is a _text editor_.
Text editors are applications that help you write code.

It's important to note the difference between a text editor and a word
processor, like Microsoft Word or Google Docs. Text editors are designed to
work with plain text, like code and markup languages.
Word processors are designed to work with rich text that may include fonts,
colors, and graphics. It's difficult (but not impossible) to create one type of
text with the tool designed for the other, but just as a screwdriver can
sometimes be used as a hammer, it's not the best choice.

<!-- Todo: update image URL -->

<a href="https://code.visualstudio.com/">
    <img align="right" style="margin:10px 0 10px 10px" width="20%"
    src="./media/Visual_Studio_Code_1.35_icon.svg.png"> </a>

There are a wide variety of free and open source text editors available
for download.
We recommend [Visual Studio Code][vs-code] (VS Code) from Microsoft.

VS Code is available for Linux, macOS, and Windows.
Please click the logo image on the right (or use the link above) to download,
then install, VS Code on your computer.

Once installed, you can run VS Code from the Start menu on Windows, from the
Applications directory on macOS, and from the applications menu on a Linux
distribution.

---

La última aplicación que necesitamos para completar nuestro entorno de
programación científica es un _editor de texto_.
Los editores de texto son aplicaciones que te ayudan a escribir código.

Es importante tener en cuenta la diferencia entre un editor de texto y un
procesador de textos, como Microsoft Word o Google Docs.
Los editores de texto están diseñados para trabajar con texto sin formato, como
código y lenguajes de marcado.
Los procesadores de texto están diseñados para trabajar con texto enriquecido
que puede incluir fuentes, colores y gráficos.
Es difícil (pero no imposible) crear un tipo de texto con la herramienta
diseñada para el otro, pero así como un destornillador a veces puede usarse
como un martillo, no es la mejor opción.

Hay una amplia variedad de editores de texto gratuitos y de código abierto
disponibles para descargar.
Recomendamos [Visual Studio Code][vs-code] (VS Code) de Microsoft.

VS Code está disponible para Linux, macOS y Windows.
Haga clic en la imagen del logotipo a la derecha (o use el enlace de arriba)
para descargar e instalar VS Code en su computadora.

Una vez instalado, puede ejecutar VS Code desde el menú Inicio en Windows,
desde el directorio de aplicaciones en macOS y desde el menú de aplicaciones en
una distribución de Linux.

# Project Jupyter | Proyecto Jupyter

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
abierto e impulsada por la comunidad, que supervisa el desarrollo de un
ecosistema de software para programación científica interactiva, el aprendizaje
y el descubrimiento.
El proyecto Jupyter surgió del [proyecto IPython][ipython] iniciado por Fernando
Pérez cuando era estudiante de posgrado en física en la Universidad de
Colorado Boulder.

En CoCo, usaremos tres herramientas del ecosistema Jupyter:
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

[JupyterHub](https://jupyter.org/hub) es un servicio que permite que
múltiples usuarios accedan a recursos computacionales, donde cada usuario
puede ejecutar Jupyter Notebook y otro software en su propio espacio de trabajo.
Un JupyterHub se puede instalar en la nube o localmente.

A través del proyecto [OpenEarthscape][oes] financiado por la NSF,
el [Community Surface Dynamics Modeling System][csdms] (CSDMS) proporciona un
[JupyterHub][csdms-jhub] donde se pueden ejecutar los Notebooks de CoCo.
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

JupyterLab es un entorno de desarrollo interactivo que se utiliza desde el navegador.
Proporciona herramientas para escribir código y crear notebooks, como también:

- un explorador de archivos,
- lanzadores para notebooks, archivos de datos e imágenes,
- aplicaciones de terminal, editor de texto, y
- atajos de teclado para acelerar su trabajo.

JupyterLab es la interfaz predeterminada de JupyterHub.
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

Un Jupyter Notebook es un documento interactivo para escribir, explicar y ejecutar
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

## Resources | Recursos

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

# Summary | Resumen

The software we've installed--a Python distribution, a terminal application,
and a text editor--form the basis of a scientific coding environment.
We will do more work to configure this scientific coding environment as we
progress through CoCo.
By the end, you will be able to use these tools in your research, and they'll
live on your computer long after the last CoCo lesson.

---

Los softwares que hemos instalado (una distribución de Python, una aplicación
de terminal y un editor de texto) forma la base de un entorno de programación
científica.
Haremos más trabajo para configurar este entorno de programación científica a
medida que avanzamos en CoCo.
Al final, podrá usar estas herramientas en su investigación y permanecerán en
su computadora mucho después de la última lección de CoCo.

# Homework | Tarea

After completing this lesson,
please try to install

* Anaconda,
* Git for Windows (Windows only), and
* VS Code

on your computer using the information above.


<!-- Links, by alpha -->

[badge]: https://img.shields.io/badge/CSDMS-JupyterHub-orange.svg
[anaconda-distribution]: https://www.anaconda.com/products/distribution
[csdms]: https://csdms.colorado.edu
[csdms-jhub]: https://lab.openearthscape.org
[csdms-jhub-link]: https://lab.openearthscape.org/hub/user-redirect/git-pull?repo=https%3A%2F%2Fgithub.com%2FCodeToCommunicate%2FCoCoLessons&urlpath=lab%2Ftree%2FCoCoLessons%2F%3Fautodecode&branch=main
[git-for-windows]: https://gitforwindows.org/
[git-install-instructions]: https://carpentries.github.io/workshop-template/#shell
[ipython]: https://ipython.org/
[jupyter]: https://jupyter.org/
[jupyterhub-docs]: (https://jupyterhub.readthedocs.io)
[jupyterlab-docs]: (https://jupyterlab.readthedocs.io)
[jupyter-notebook-docs]: https://jupyter-notebook.readthedocs.io
[oes]: https://openearthscape.org/
[swc-ppp]: https://swcarpentry.github.io/python-novice-gapminder/
[swc-ppp-1]: https://swcarpentry.github.io/python-novice-gapminder/01-run-quit/index.html
[vs-code]: https://code.visualstudio.com/
