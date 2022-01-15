![CoCo logo](https://github.com/CodeToCommunicate/CoCoLessons/blob/main/media/coco-banner.jpg)

# Project Jupyter

<a href="https://jupyter.org/"><img style="float: right; width: 15%; margin: 0 0 0 20px" src="https://jupyter.org/assets/homepage/main-logo.svg"></a>

[Project Jupyter][jupyter] is a non-profit, open-source, community-driven project that oversees the development of a software ecosystem for interactive scientific coding, learning, and discovery.
Project Jupyter grew out of the [IPython project][ipython] started by Fernando P&eacute;rez when we was graduate student in physics at the University of Colorado Boulder.

In CoCo,
we'll use three tools from the Project Jupyter ecosystem:
JupyterHub, JupyterLab, and Jupyter Notebook.


## JupyterHub

A [JupyterHub](https://jupyter.org/hub) is
a server that allows multiple users
access to a computational resource.
Each user can run Jupyter Notebook
and other software in their own workspace.
A JupyterHub can be installed in the cloud or locally.

Through the NSF-funded [OpenEarthscape][oes] project,
the [Community Surface Dynamics Modeling System][csdms] (CSDMS)
provides a [JupyterHub][csdms-jhub] where CoCo notebooks can be run.
Click this button [![Run on CSDMS JupyterHub][badge]][csdms-jhub-link]
to open the CoCo lessons directly on the CSDMS JupyterHub!


## JupyterLab

JupyterLab is a web-based interactive development environment


## Jupyter Notebook

Jupyter Notebook is ...

an interactive environment for writing and running code.

https://www.dataquest.io/blog/jupyter-notebook-tutorial/

IPython is a powerful Python REPL that gives you tab completion, better tracebacks, multiline editing, and several useful features on top of pure Python Scripts. It is also the library that powers the Jupyter Kernel via the IPykernel.

Wikipedia:

> Jupyter Notebook (formerly IPython Notebooks) is a web-based interactive computational environment for creating notebook documents.

> A Jupyter Notebook document is a browser-based REPL containing an ordered list of input/output cells which can contain code, text (using Markdown), mathematics, plots and rich media. Underneath the interface, a notebook is a JSON document, following a versioned schema, usually ending with the ".ipynb" extension. 

## Resources

* [Project Jupyter](https://jupyter.org/)
* [JupyterHub documentation](https://jupyterhub.readthedocs.io)
* [JupyterLab documentation](https://jupyterlab.readthedocs.io)
* [Jupyter Notebook documentation](https://jupyter-notebook.readthedocs.io)
* A collection of [notable Jupyter Notebooks](https://github.com/jupyter/jupyter/wiki)


<!-- Links, by alpha -->

[badge]: https://img.shields.io/badge/CSDMS-JupyterHub-orange.svg
[csdms]: https://csdms.colorado.edu
[csdms-jhub]: https://lab.openearthscape.org
[csdms-jhub-link]: https://lab.openearthscape.org/hub/user-redirect/git-pull?repo=https%3A%2F%2Fgithub.com%2FCodeToCommunicate%2FCoCoLessons&urlpath=lab%2Ftree%2FCoCoLessons%2F%3Fautodecode&branch=main
[ipython]: https://ipython.org/
[jupyter]: https://jupyter.org/
[oes]: https://openearthscape.org/
