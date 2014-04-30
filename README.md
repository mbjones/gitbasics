---
title: Git Basics
author: Matt Jones
---

![](version-graph.png =250x)

## Why version control, and why Git?

- Save time
- Make changes with confidence
- Reuse your work
- Collaborate with others

## Some examples

- [Sean Anderson](https://github.com/seananderson)
- [ROpensci rFishbase](https://github.com/ropensci/rfishbase)

## A quick demo tutorial

- [Code School tutorial](http://try.github.io/)

## Installing Git and related software

### Mac OS X

- Open 'Terminal'
- Check if 'git' is installed
- If not, install from: [Git for Mac](http://git-scm.com/download/mac)
- Before running the first time, you must configure your name and email:

``` {.bash}
git config --global user.name "Matt Jones"
git config --global user.email "jones@nceas.ucsb.edu"
```

- Optional: Install [TextMate](https://api.textmate.org/downloads/release), and configure it as the editor for git commit messages

```bash
git config --global core.editor 'mate -w'
```

### Windows

- Install [Git Bash](http://msysgit.github.io/)

```bash
git config --global user.name "Matt Jones"
git config --global user.email "jones@nceas.ucsb.edu"
git config --global core.editor '"C:\Program Files (x86)\Windows NT\Accessories\wordpad.exe"'
```

## Topics

- Version control systems
- Creating a repository
- Adding and committing files
- Working with remote repositories
- Using tags
- Branching and merging

## Typical workflow

```bash
mkdir test
cd test
echo "This is a test file." > README.txt

# Initialize the git repository and start tracking files
git init
git status
git add README.txt
git status
git commit -m "Initial draft of README."

# Make some changes to the file and commit them
echo "===================" >> README.txt
git status
git add README.txt
git status
git commit -m "Added formatting."

# View the history of changes
git log
git blame README.txt
```

## Working with remote repositories

Use `git clone` to copy a remote repository to your local host, and then use `git push` to write your changes back up to the repository.

```bash
git clone git@github.com:mbjones/pgame.git
git remote -v
git pull origin master
echo " " >> README.md
git add README.md
git commit -m "Added a newline to end of Readme."
git status
git push origin master
```
