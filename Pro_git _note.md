# Chapter 2 (Git basic)
## get a repository(repo)
1. init a repo in an exiting dir
- used for not under control
- ```$ cd C:/Users/dell/project_name``` and ```git init```(this will create a new subdir named .git containing all repo files)
- to control exiting file
``` shell
$ git add *.c 
$ git add LICENSE 
$ git commit -m 'Initial project vers'
```
2. clone an existing repo
```shell
$ git clone [url] dir_name(optional)
```
- the dir_name is the name you want the file to be
- open your vpn to all

## recording change to the repo
files of 4 kinds: untracked,{ unmodified, modified, staged}(tracked)
- modified files need to be staged(use add) to be the stage file
- untracked files can be added to be the staged file,
- staged files need to be committed to be an unmodified file
- a tracked file being modified can turn into an modified file
1. to know the stage of the dir and all the files
```shell
$ git status
```
```shell
$ git status -s
``` 
simplified version
2. short cut
- aren't tracked '??'
- new file added to staging 'A'
- modified file 'M'
- staged and then modified again 'MM'
3. .gitignore place where you tell git to ignore the kinds of files you do not want to track, see the example in .gitignore or the [net](https://github.com/github/gitignore)
4. 