# yorick: a project skeleton / template / boilerplate tool

Whenever we start a programming project (or a book, or anything you do that involves files on a computer), we often end up doing the same initial steps, without much variation.

Yorick allows you to automate this by creating "skeletons" - templates that you can "construct" to create a boilerplate project. In the process of constructing, a skeleton can prompt the user for variables (project name, for instance), and have those variables substituted appropriately into the 

A collection of skeletons for different types of projects is called a "closet". Yorick automatically gives you a default closet to keep all of your own skeletons in, and the ability to add other people's closets alongside it. You can keep your closet to yourself or open it up to the world on GitHub (a bit like dotfiles).

## Installation

1. You need to have Python installed. (If you're not a Python programmer, don't worry, you can create and use yorick skeletons without writing a single line of Python.)
	- If you use Linux or OS X, you probably already have it. Run `python --version` to make sure it's version 2.7 - if not, 

## Usage

### Constructing a project

Projects are constructed using the `yorick construct` command.

```shell
$ yorick construct example
Enter a name for your project.
project_name> spam
Constructing... Done.

$ find .
./spam/
./spam/__init__.py
./README.md

$ cat README.md
# spam

Insert a readme for spam here.
```

Skeletons are specified in the form `yorick construct <closet-alias>.<skeleton-name>`. (Closet aliases are covered below.) If the closet alias is left out, as with `yorick construct example` above, the skeleton is taken from the `__default__` closet.

If your skeleton isn't in a closet, use the `-p` flag to specify a path to it, for example `yorick construct -p ~/blah/myskeleton`.

### Installing somebody else's closet

Closets are shared as Git repositories or tarballs, and added with the `yorick install-closet` command. They can be updated with the `yorick update-closets` command.

```shell
$ yorick install-closet --git http://github.com/adambrenecki/yorick-closet abre
Waiting on VCS... Done.
You can now install a skeleton from this closet by running 'yorick construct abre.<skeleton-name>'

$ yorick update-closets
Updating abre... Done.
```

### Creating a skeleton

Use the `yorick create-skeleton` command to create a new skeleton.

```shell
$ yorick create-skeleton
Enter a name for your skeleton.
skeleton_name> eggs
Enter the closet to put your skeleton in.
closet [leave blank for __default__]>
Constructing... Done.
You can now edit your skeleton at ~/.yorick/__default__/eggs/
```


#### Configuration Files and Variables

Open the `config.yml` file in the `-yorick-meta` directory.

#### File names

#### File Contents



 