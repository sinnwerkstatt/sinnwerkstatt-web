# Git

http://git-scm.com/

## Introduction
* [git - Der einfache Einstieg ](http://rogerdudler.github.io/git-guide/index.de.html)
* [Learn Git Branching](http://pcottle.github.io/learnGitBranching/)

## Windows
Here are described the steps to use Git under Windows. Feel free to improve the documentation.

* [Create a github account](https://github.com/signup/free)
* Install [msysgit](http://msysgit.github.com/)
* Install [TortoiseGit](http://code.google.com/p/tortoisegit/)
* Generate [a new RSA Key with TortoiseGit](http://uncod.in/blog/setting-up-a-github-account-on-windows7/)
* Check this [basic tutorial](http://uncod.in/blog/github-tortoisegit-and-organizational-workflow-tutorial/) on Cloning, Adding, Commiting, Pushing and sending Pull request.

## Links
* Tutorials:
    * http://www.vogella.com/articles/Git/article.html
* Git Help: http://help.github.com/
* Git Extras: https://github.com/visionmedia/git-extras

## Github
* SSH Key: https://help.github.com/articles/generating-ssh-keys
* [GitHub Trends](https://github.com/trending)
* [Inside GitHub](http://www.slideshare.net/rubymeetup/inside-github-with-chris-wanstrath)

## Commands

### Commits
* [A Better Git Commit](http://web-design-weekly.com/blog/2013/09/01/a-better-git-commit/)

### Branches
* Create and switch to a new branch: ```git checkout -b branch_name```
* Create and switch to a new branch: ```git checkout -b branch_name origin/branch```
* Switch to a branch: ```git checkout branch_name```
* Delete a branch: ```git branch -d branch_name```
* Rename branch: ```git branch -m new_branch_name```

## When merge branch was accepted
* ```git remote update``` (get and update all remote references)
* ```git remote prune origin```  (remove all local references to remote branches of origin)
* ```git branch -av``` (view all branches)
* ```git checkout master``` (change to your local branch)
* ```git pull```
* ```git branch -d branch_name``` (delete the local branch)

### Overwrite local files with master
* ```git fetch origin master```
* ```git reset --hard FETCH_HEADv
* ```git clean -df```

## Cheat Sheet
* [Git-Cheat-Sheet.pdf](https://github.com/AlexZeitler/gitcheatsheet/blob/master/gitcheatsheet.pdf?raw=true) ([Source](https://github.com/AlexZeitler/gitcheatsheet))

## Workflow
* http://scottchacon.com/2011/08/31/github-flow.html

## Links
* [Quickly publish Github pages](http://pages.github.com/)
