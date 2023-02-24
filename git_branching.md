# Git branching 
## start a new branch
branches work like pointers to different version, the master branch is initiated automatically and move to the most recent version of the snapshot. We can create other branches to point to those versions that branching out from the main trunk. HEAD is the pointer showing  where you are currently point to.  
1. start a branch
```shell
$ git branch branchname
```
or 
```shell 
$ git checkout -b branchname
```
the second one will automatically switch to the new branch  
without the -b, it will create a new tag
2. delete a branch
```shell
$ git branch -d branchname
```
3. switch the branch 
```shell
$ git checkout branchname
```
4. more info about the branch
```shell
$ git log
```
## 
