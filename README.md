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

## Collaboration

main branch is like main trunk of tree, branch allows to branch off from main
tree trunk.

- git bracnh:

  - git branch->this will give list of all branch in current project
  - git branch -M main-> this will rename branch to main
  - git branch <branch name> ->this will create new branch
  - git branch -d/-D <branch name> -> this delete the branch

- git checkout:

  - git checkout <branch name> -> this will take us to that branch

- Merge conflicts
  it occurs when we try to merge two diff branches and they modify the same lines of code

  - git diff-> Used to compare the changes in the feature branch and master branch
  - The easiest way to fix the merge conflict is use the editor to choose between the incoming changes (feature) or the existing changes (master). Then create a new merge commit with the changes you want to keep.
  - git merge --abort-> If not sure, we can abort

- Fork

  - when we fork a repo it will copy that repo to my account
  - this allow us to make changes to it without affecting the original repo
  - at same time it maintains a link to original repo where we can fetch updates
  - original repo is known as upstream repo

- Pull Request

  - it is way to submit contribution to another repo
  - Fork a repo-> create a copy of another user's repo
  - download a remote repo to local machine
  - create a branch and make req changes (add->commit->push)
  - git remote add upstream <link of forked repo>-> this will keep us insink with original
  - git fetch upstream-> to download the changed and git rebase upstream/master->to add those changes to top of our work

## Other features

We have three diff files area in git
current working dir, Staging area, commits

- git reset

  - git reset-> this will Unstage all staged files
  - git reset <commit-ID> -> Rollback to a previous commit, but keep changes in the working directory
  - git reset <commit-ID> --hard -> Rollback to a previous commit AND discard all changes
  - git reset should not be used when commit is pushed to remote repo

- git revert

  - git revert <commit-ID> -m "reverting last commit" -> Undo a commit with a new commit
  - git revert Undo's a commit with out changing the course of history

- git commit -- ammend

  - git commit --amend -m "better message"-> this Update the message on your last commit
  - git add <your-file> followed by git commit --amend --no-edit -> this will include a file you forgot on your last commit

- git stash
  this allows to save work without commiting it to repo commit history

  - git stash -> this creates a stash, git stash pop-> this will get back
  - git stash save <name>-> this Manages all stashes more easily by giving them a name
  - git stash list-> this List out all stashes
  - git stash apply <index>-> this Apply a stash based on its index

- git rebase
  this allows to merge updates with a clean commit history, this keeps feature branch upto date with master branch

  - git checkout feature followed by git rebase master-> From a feature branch, rebase the latest changes from the master branch

- git squash
  take multiple of commits and combine to one single commit
  - git rebase master --interactive-> this will Start an interactive rebase from a feature
  - now choose the squash commend to flatten your commits into a single message

## GitHub Actions
