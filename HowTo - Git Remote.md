
# HowTo - Git Remote

REF.: [1] [Git - git-remote Documentation](https://git-scm.com/docs/git-remote)  
REF.: [2] [Git - Working with Remotes](https://git-scm.com/book/en/v2/Git-Basics-Working-with-Remotes)  

----

## Adding a Remote Repository

```bash
git remote add <name> https://path-to/the-project.git
# Note: As a common naming convention "origin" is often used for
# the default remote repository; change this name when you
# add more remote repositories.
```

## Changing a Remote's URL

```bash
git remote set-url origin https://path-to/the-project.git
# Remember "origin" is just a name
```

## Listing Existing Remotes

```bash
$ git remote
origin
$ git remote -v
origin  https://path-to/the-project.git (fetch)
origin  https://path-to/the-project.git (push)
```

## Renaming a Remote

```bash
git remote rename <old_name> <new_name>
```

## Removing a Remote

```bash
git remote remove <name>
```

## Inspecting a Remote

```bash
git remote show origin
# "It lists the URL for the remote repository as well as the
# tracking branch information." [2]
```
