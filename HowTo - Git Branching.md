# HowTo - Git Branching

:link: [Git Book - 3.1 Git Branching - Branches in a Nutshell](http://book.git-scm.com/book/en/v2/Git-Branching-Branches-in-a-Nutshell#ch03-git-branching)

----

### Creating a New Branch

```git
git branch <new-branch-name>
```

### Creating a New Branch up to a Specific Commit

```git
git branch <new-branch-name> <commit-hash>
```

### Switching Branches

```git
git checkout <branch-name>
```

_or_ (Git v2.23+)

```git
git switch <branch-name>
```

### Creating and Switching to a New Branch

```git
git checkout -b <new-branch-name>
```

_or_ (Git v2.23+)

```git
git switch -c <new-branch-name>
git switch --create <new-branch-name>
```

### Return to Previous Branch

```git
git checkout <other-branch-name>
```

_or_ (Git v2.23+)

```git
git switch -
```

### Merging Changes to the Main Branch

```git
git checkout main
git merge <branch-name>
```

### Deleting a Branch

```git
git branch -d <branch-name>
```

### Changing a Branch Name

```git
git branch -M <old-branch-name> <new-branch-name>
git branch --move <old-branch-name> <new-branch-name>
```

_Let others see the corrected branch on the remote:_

```git
git push --set-upstream origin <new-branch-name>
git push origin --delete <old-branch-name>
```

### Listing Branches

Examples:

```git
git branch
git branch -v
git branch --merged
git branch --no-merged
git branch --no-merged master
git branch --all
```

----

### Basic Merging Conflicts

A graphical tool to resolve merging issues:

```git
git mergetool
```

