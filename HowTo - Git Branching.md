# HowTo - Git Branching

:link: [Git Book - 3.1 Git Branching - Branches in a Nutshell](http://book.git-scm.com/book/en/v2/Git-Branching-Branches-in-a-Nutshell#ch03-git-branching)

----

## Creating a New Branch

```shell
git branch <new-branch-name>
# creating a New Branch up to a Specific Commit
git branch <new-branch-name> <commit-hash>
```

### Creating and Switching to a New Branch

```shell
git checkout -b <new-branch-name>
# or (Git v2.23+)
git switch -c <new-branch-name>
git switch --create <new-branch-name>
```

## Switching Branches

```shell
git checkout <branch-name>
# or (Git v2.23+)
git switch <branch-name>
```

### Return to Previous Branch

```shell
git checkout <other-branch-name>
# or (Git v2.23+)
git switch -
```

## Merging Changes to the `main` Branch

```shell
git checkout main
git merge <branch-name>
```

## Deleting a Branch

```shell
# local
git branch -d <branch-name>
# remote
git push origin –d <branch-name>
```

## Renaming a Branch

```shell
git branch -M <old-branch-name> <new-branch-name>
git branch --move <old-branch-name> <new-branch-name>
```

_Let others see the corrected branch on the remote:_

```shell
git push --set-upstream origin <new-branch-name>
git push origin --delete <old-branch-name>
```

## Listing Branches

Examples:

```shell
# local branches
git branch
git branch -l
git branch --list
# local branches with each last commit
git branch -v
# local branches with each last commit and upstream branch
git branch -vv
# local branches which have merged with current/given branch
git branch --merged
git branch --merged <branch-name>
# local branches which have NOT merged with current/given branch
git branch --no-merged
git branch --no-merged <branch-name>
# branches with/without specific/last commit
git --contains [<commit>]
git --no-contains [<commit>]
# local and remote branches
git branch -a
git branch --all
# remote branches only
git branch -r
git branch --remotes

```

----

### Basic Merging Conflicts

A graphical tool to resolve merging issues:

```shell
git mergetool
```
