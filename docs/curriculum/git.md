# Git & Github

## Overview

`git` is a decentralized version control system:  

* helps you not lose your code!
* track and merge concurrent changes to a repository of files
* collaborate with several authors
* decentralized across machines (can push & pull changes from several remote repositories)
* `git` is the CLI, GUIs exist

[github.com](https://github.com) is a popular host of git repositories.

## `git` basics

Git represents 

* commits
* branches
* useful refs

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

## Exercise

1. Install a git client
1. Make a GitHub account
1. Fork this repository
1. Add your name and a short description about yourself to [the contributors page](../../contributors)
1. Make a pull request against this repository!

Resources:  

* https://help.github.com/en/articles/set-up-git
* https://gist.github.com/derhuerst/1b15ff4652a867391f03
* https://lab.github.com/githubtraining/introduction-to-github
