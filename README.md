# GitHub & Git Foundation

- [GitHub & Git Foundation](#GitHub--Git-Foundation)
  - [Setup](#Setup)
    - [Init a normal repository](#Init-a-normal-repository)
    - [Init a bare (naked) repository](#Init-a-bare-naked-repository)
    - [create a new repository on the command line](#create-a-new-repository-on-the-command-line)
    - [push an existing repository from the command line](#push-an-existing-repository-from-the-command-line)
  - [Configurations](#Configurations)
    - [Config the user name and email](#Config-the-user-name-and-email)
      - [In gloabal](#In-gloabal)
      - [In local](#In-local)
    - [Setting colors](#Setting-colors)
    - [Cheking logs](#Cheking-logs)
  - [Commit](#Commit)
    - [Check status](#Check-status)
    - [Add files into staging area](#Add-files-into-staging-area)
    - [Commit files](#Commit-files)
  - [Diff](#Diff)
    - [Diff comparing the current working to the staged](#Diff-comparing-the-current-working-to-the-staged)
    - [Diff comparing the staged area to the last commit](#Diff-comparing-the-staged-area-to-the-last-commit)
    - [Diff comparing current working to the HEAD](#Diff-comparing-current-working-to-the-HEAD)
    - [Stylish Diff commands](#Stylish-Diff-commands)
    - [Diff in status](#Diff-in-status)
  - [Log](#Log)
    - [Log in the most easy way](#Log-in-the-most-easy-way)
    - [Log in one line or / and with stats](#Log-in-one-line-or--and-with-stats)
    - [Log with chained parameters](#Log-with-chained-parameters)
  - [Remove](#Remove)
    - [Remove file from the stage](#Remove-file-from-the-stage)
    - [Remove deleted file](#Remove-deleted-file)
    - [Update all tracked files (most commonly used)](#Update-all-tracked-files-most-commonly-used)
    - [Remove file from cached / stage](#Remove-file-from-cached--stage)

## Setup

### Init a normal repository

In case for a normal repository, which is usually applied in a develope directory. This is a very commonly used with GitHub or custom git server together.

```Git
git init
```

### Init a bare (naked) repository

In case for a shared / team repository. Normally used in a custom git server.

```Git
git init --bare
```

### create a new repository on the command line

```Git
echo "# learngithub" >> README.md
git init
git add README.md
git commit -m "first commit"
git remote add origin <origin>
git push -u origin master
```

### push an existing repository from the command line

```Git
git remote add origin <origin>
git push -u origin master
```

## Configurations

### Config the user name and email

#### In gloabal

```Git
git config --global user.name

git config --global user.email

```

#### In local

```Git
git config --local user.name <user name>

git config --local user.email <user email>
```

### Setting colors

```Git
git config --global core.autocrlf true

git config --global core.autocrlf input

git config --global color.ui auto

```

### Cheking logs

```Git
git log
```

## Commit

### Check status

```Git
git status
```

### Add files into staging area

```git
git add <file>
```

### Commit files

```git
git commit -m "<description>"
```

## Diff

### Diff comparing the current working to the staged 

### Diff comparing the staged area to the last commit

To see what staged changes are made to the last local commit, "**--staged**" means the status after **git add**.

```git
git diff --staged

git diff --cached
```

### Diff comparing current working to the HEAD

To see what current changes in working, no matter staged or unstaged, are made to HEAD, which means the recently last commit

```git
git diff HEAD
```

### Stylish Diff commands

To check the difference in words

```git
git diff --color-words
```

### Diff in status

To return the differences of status

```git
# current working against staged (default)
git diff --stat
# staged against last local commit
git diff --cached --stat
# current working against last local commit
git diff HEAD --stat
```

## Log

### Log in the most easy way

```git 
git log
```

This command shows all logs from the latest to the oldest in timeline.

### Log in one line or / and with stats

```git
# log in one line, only shortend commit ref and message
git log --oneline
# log with stats, all invloved files.
git log --stat
# log in oneline and with stat
git log --oneline --stat
```

### Log with chained parameters

```git
git log --graph --all --decorate --oneline 
```

## Remove

### Remove file from the stage

```git
git rm file1.txt
```

> Note:
> With using the command above, "file1.txt" is only removed from cache/stage. The branch will not be affected, until "**git commit**" is called. By "**git status**", the removed / deleted files will be displayed, before commit.

```git
#remove
git rm file1.txt
#check
git status
#commit
git commit -m "Remove file1.txt"
```

### Remove deleted file

```git
# delete from file system
rm file2.txt
# check status
git status
# even the file is deleted, it can still be removed from stage 
git rm file2.txt
```

### Update all tracked files (most commonly used)

which also means all delted files can be removed, if they have been tracked before. However, the modification in other tracked files will be updated, too.

```git
git add -u
# or for the current path
git add -u .
```

### Remove file from cached / stage

```git
git rm --cahced file3.txt
```

> Note: The file was not removed from file system. Instead it is no more tracked by **git**.

