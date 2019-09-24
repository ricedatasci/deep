# Git & Github

## Overview

`git` is a decentralized version control system:  

* helps you not lose your code!
* track and merge concurrent changes to a repository of files
* collaborate with several authors
* decentralized across machines (can push & pull changes from several remote repositories)
* `git` is the CLI, GUIs exist

[github.com](https://github.com) is a popular host of git repositories.

## Basics of Version Control with `git`

`git` uses a [merkle-tree](https://en.wikipedia.org/wiki/Merkle_tree) to track
diffs.  A commit represents a diff between two states of the repository.  A
commit hash is composed of the data composed in the diff and the previous
commit's hash.

```shell
$ # make changes to some files
$ git add models/cnn.py optimizers/adam.py
$ git commit -m "CNN: added 4th convolution block and fixed Adam convergence issue"
```

Commits are chained together in branches.  Branches can exist alongside
each other and generally represent new features or ideas.

```shell
$ git checkout -b "sift-feature-extraction"
$ # add code to use SIFT features
$ git commit "feat-ex: Implemented SIFT to extract local image features"
```

After you've done some work, you'll generally push up to github.com or another
repository host! Generally you'll set up git remotes when cloning or
initializing a project, so that you can push like so:

```shell
$ # after you've committed all your work
$ # origin is a common name for the default remote
$ git push origin sift-feature-extraction
```

## GitHub

In addition to hosting git repositories, GitHub offers collaborative features
such as issue tracking & pull requests.  Pull requests are essentially a
request to merge changes from a downstream fork to an upstream repo.  

### forking

Forking `foo/repository` create's a new repo, `repository`, under your
account with the same git history as `foo/repository`.

### pull requests

To suggest changes to repositories on github the most common workflow is to
fork the repository, make changes on your fork, and make a pull request from
your branch onto an upstream branch.  

Example:  Alice has a collection of machine learning algorithms in
alice/machine-learning.  Bob would like to add an example of a deep neural
network to Alice's repository.  Bob forks alice/machine-learning to
bob/machine-learning, and pushes his changes to the DEEP branch on
bob/machine-learning.  Bob then makes a pull request from bob/machine-learning
to alice/machine-learning.
