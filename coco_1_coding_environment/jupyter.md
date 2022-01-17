![CoCo logo](./media/coco-banner.jpg)

# Project Jupyter

<img align="right" width="150" height="150" src="https://jupyter.org/assets/homepage/main-logo.svg">

[Project Jupyter][jupyter] is a non-profit, open-source, community-driven organization that oversees the development of a software ecosystem for interactive scientific coding, learning, and discovery.
Project Jupyter grew out of the [IPython project][ipython] started by Fernando P&eacute;rez when we was a graduate student in physics at the University of Colorado Boulder.

In CoCo,
we'll use three tools from the Project Jupyter ecosystem:
JupyterHub, JupyterLab, and Jupyter Notebook.


## JupyterHub

A [JupyterHub](https://jupyter.org/hub) is
a server system that allows multiple users
access to a computational resource,
where each user can run Jupyter Notebook
and other software in their own workspace.
A JupyterHub can be installed in the cloud or locally.

Through the NSF-funded [OpenEarthscape][oes] project,
the [Community Surface Dynamics Modeling System][csdms] (CSDMS)
provides a [JupyterHub][csdms-jhub] where CoCo notebooks can be run.
Click this button [![Run on CSDMS JupyterHub][badge]][csdms-jhub-link]
to open the CoCo lessons directly on the CSDMS JupyterHub!


## JupyterLab

JupyterLab is a browser-based interactive development environment.
It provides tools for
writing code and creating notebooks,
including
* a file browser,
* launchers for notebooks, data files, and images,
* terminal, text editor, and code console applications, and
* keyboard shortcuts to speed your work.

JupyterLab is the default user interface for JupyterHub.
Like JupyterHub,
JupyterLab can be installed in the cloud or locally.


## Jupyter Notebook

A Jupyter Notebook is an interactive document for writing, explaining, and running code,
and for communicating results.

Notebooks are live documents,
with the ability to display graphics and tabular data,
as well as interactive displays with widgets.
A notebook is made of cells.
Each cell can hold code, text (using Markdown), equations, or visualizations.

To get a sense of their popularity,
by [one estimate](https://github.com/parente/nbestimate/blob/master/estimate.ipynb),
there are currently over 7.5 million notebooks currently hosted on GitHub.
The estimate is presented, of course, in a notebook.


## Resources

* [Project Jupyter][jupyter]
* JupyterHub [documentation][jupyterhub-docs]
* JupyterLab [documentation][jupyterlab-docs] and [an entertaining demonstration](https://youtu.be/A5YyoCKxEOU) on YouTube
* Jupyter Notebook [documentation][jupyter-notebook-docs]
* A collection of [notable Jupyter Notebooks](https://github.com/jupyter/jupyter/wiki) and a comprehensive [tutorial](https://www.dataquest.io/blog/jupyter-notebook-tutorial/)


___

[Setting up a scientific coding environment](./index.md) |
Previous: [index](./index.md) |
Next: [Introduction to the shell](./shell-intro.md)


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
