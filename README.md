# GitHub & Git Foundation

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

```Git
git config --global user.name

git config --global user.email

```

### Setting colors

```Git
git config --global core.autocrlf true

git config --global core.autocrlf input

git config --global color.ui auto

```

