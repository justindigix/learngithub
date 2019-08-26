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
