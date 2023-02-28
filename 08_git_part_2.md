# Git part 2

- Recopilacion de lo que aprendieron sobre la rama y los commit
- como es el flow par acreara una rama y porque se hace
- como creo una rama
- trabajar en esta nueva rama
- volver a la main
- traer los cambion a la main
- Subri todo a gitgub
- Mostrar el mismo flow pero usando github y los PR
- https://github.com/santisoler/git-intro-geolatinas/blob/main/content.md
- https://swcarpentry.github.io/git-novice/

<img align="center" style="margin:0 0 20px 0" width="100%" height="100%" src="https://raw.githubusercontent.com/CodeToCommunicate/CoCoLessons/main/media/coco-banner.jpg">

# Working with branches | Trabajando con ramas

## Resumen hasta el momento

- Sabemos como trabajar en la rama _main_.

  - Los cambios se guardan en el repositorio como _commits_ (`git add` y `git
commit`).
    <img src="data/git/git-staging-area.svg" alt="" style="height: 85vh">

- Sabemos crear repositorios remotos en GitHub.

  - Sabemos como subir (`git push`) y traer (`git pull`) cambios de entre nuesto
    repositorio local y remoto.
    <img src="data/git/github-repo-after-first-push.svg" alt="" style="height: 85vh">

**El maximo explendor de _Git_ se obtiene cuando empezamos a trabajar con ramas
dentro de nuestro repositorio.**

## ¿Qué es una rama y como se trabaja con ella?

Branches are one of the core concepts in Git.
And there's an endless amount of things you can do with them.
One of the most important functions of Git is the control of branches of
development that help improve the creation of a project.

_Git branches_ help us have multiple versions of an project organized.
That’s why working with them is very important.

Using Git development branches is a pretty great way to work with our
application while tracking its versions.
In general, a development branch is a bifurcation of the state of code that
creates a new path for the evolution of it.
It can be parallel to other Git branches that you can generate.
As we can see, it is possible to incorporate new functionalities to our
code/project in an orderly and precise way.

For example, suppose our repository has 4 commits on the `main/master` branch:
<img src="data/git/git-repo-2.svg" alt="" style="height: 85vh">

Then we find a bug in our code/project and we want to fix it, but we are not
sure how.
So, we create a new branch to try different ways to fix it.
Therefore we create a new branch called `fix-bug`:
<img src="data/git/git-repo-3.svg" alt="" style="height: 85vh">

In this new branch we make several commit to fix bug. At the same time we make
other commit in the `main` branch:
<img src="data/git/git-repo-5.svg" alt="" style="height: 85vh">

Now that we could fix the bug in the `fix-bug` branch, we want to add these
commit to the `main` branch using the `git merge` command:
<img src="data/git/git-repo-6.svg" alt="" style="height: 85vh">

### Ventajas de usar ramas

Using Git Branches has multiple advantages.
However, we want to emphasize the following two:

- It is possible to develop new features for our project without hindering
  the development in the main branch.
- With Git branches it is possible to create different development branches
  that can converge in the same repository.
  For example, a stable branch (main), a test branch, and an fix-bug branch.

Of course, each developer will be able to establish their own methods with
their own advantages using experience as a guide.

## How to Create a Branch in Git

In any Git project we can view all branches by entering the following command:

```
git branch
```

This command lists al the brnaches and put a `*` in the name of the branch that
are you located in this moment to make the changes.

Creating a branch is really simple:

```
$ git branch <new-branch-name>
```

Then, you need to move to the newly created development branch.
To do this, you will run the following command:

```
$ git checkout <new-branch-name>
```

or

```
$ git swich <new-branch-name>
```

The output will inform us that we switched to a new branch.

Now, in that new branch, we can create as many modifications as we want without
having to change anything in the main branch.
As we can see, it keeps the project organized for new modifications inclusions.

If we run the command to list the branches again, we will see that a new branch
is added and that we are located in it.

```
git branch
```

There is something we need to keep in mind if we want to make a new branch.
First, we need to commit to the main branch for Git to understand what the
main branch is.
If we do not do this, we will get an error.
So first, commit and then create the new branches.
