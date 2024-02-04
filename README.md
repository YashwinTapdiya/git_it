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

## Remote (GitHub)

- git remote:

  - this will show which remote repo is linked to local project
  - to connect local code to github-> git remote add origin https://github.com/YashwinTapdiya/git_it.git
  - git remote -v-> this will give url also
  - git remote show origin-> this provides additional info about repo

- git push:

  - this will take code in our local repo and upload it up to remote repo
  - git push -u origin master-> takes name of remote repo and branch which we want to push
  - "-u" flag is used to set origin as the upstream remote in git config so git pull can be used without any arguments in the future.

- git merge:

  - git fetch-> this fetchs changes locally
  - git merge-> it takes two diff branches and merge them together

- git pull:

  - this allows us to combine fetch + merge commands
  - if we have any uncommited changes in local repo git pull will fail(not overwrite local changes)
  - either commit the local changes first or use stash

- git clone:

  - git clone <repo link> -> this will copy all the file in remote and write them to local machine
  - it keeps reference to original repo
