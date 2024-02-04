# Learning Git

testrepo

## Editing the file

It is a markdown file in repository!!

## Lets get started

- What is git: system to keep track of changes happen accross a set of files

  - Repo - tracks the diff(changes) to codebase
  - We take snapshots/commit of the current state of the files
  - Every commit has unique id and is linked to its parent
  - We can travel back to time to previous version of our files

- Install:

  - git --version ->git version 2.40.1.windows.1
  - git config --list ->this shows the current config including username and email
  - git congig --global user.name "Yashwin Tapdiya" ->this is how to set diff field in config list

- git init:

  - this initalize a git repository
  - respository just keep track the changes in codebase

- git status:

  - tells the current state of repo
  - shows current branch and list of untracked files and changes to be commited
  - to not inculde file in repo we put that file name in .gitignore file

- git add:

  - allows to add file in staging area so that they can be included in next commit
  - git reset <filename> we can reset back to untracked

- git commit:

  - every commit has a unique id that git can use to track diff
  - git log will give id, author and time of particular commit
