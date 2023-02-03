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
4. check the difference of the content
```shell
$ git diff
```
check the difference between modified and staged
```shell
$ git diff -cached
```
check the difference between staged and unmodified
5. skip the stage step
```shell
$ git commit -a
```
this will automatically stage all the modified files
6. removing files 
```shell 
$ rm file
```
this will remove from the working dir but not staged
```shell 
$ git rm file 
```
this will remove both from the working dir and the staged place(that is the removal will be staged to commit)
```shell 
$ git rm --cached file
```
this will only remove the file from the staged place, not the working place
-> remember to add \ before the file extension, such as
```shell 
$ git rm \*.log
```
7. move the file
```shell 
$ git mv file_1 file_2
```
this will rename the file, meaning that it will move the first file to the second file, remove the first file and add the second file
## view the log
```shell
$ git log
```
optios:
1. -2: show two commit
2. --stat: show the number of lines and files edited
3. --patch: show the diff
4. --pretty=value:
5. --oneline: print in a line
6. --author:choose the author
7. --grep: search for key words
8. --since/-until: choose the time
9. -S: take a string and show the commit that change the string
10. -- path/to/file: the commit that change the specified files
11. --no-merges: ignore the merge commit
## undoing thing