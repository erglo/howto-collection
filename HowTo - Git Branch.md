# HowTo - Git Branch

REF.: [Git Book - 3.1 Git Branching - Branches in a Nutshell](http://book.git-scm.com/book/en/v2/Git-Branching-Branches-in-a-Nutshell#ch03-git-branching)

----

## Creating a New Branch

```bash
git branch <new-branch-name>
# creating a New Branch up to a Specific Commit
git branch <new-branch-name> <commit-hash>
```

### Creating and Switching to a New Branch

```bash
git checkout -b <new-branch-name>
# or (Git v2.23+)
git switch -c <new-branch-name>
git switch --create <new-branch-name>
```

## Switching Branches

```bash
git checkout <branch-name>
# or (Git v2.23+)
git switch <branch-name>
```

### Return to Previous Branch

```bash
git checkout <other-branch-name>
# or (Git v2.23+)
git switch -
```

## Merging Changes to the `main` Branch

```bash
git checkout main
git merge <branch-name>
```

## Deleting a Branch

```bash
# local
git branch -d <branch-name>
# remote
git push origin –d <branch-name>
```

## Renaming a Branch

```bash
git branch -M <old-branch-name> <new-branch-name>
git branch --move <old-branch-name> <new-branch-name>
```

_Let others see the corrected branch on the remote:_

```bash
git push --set-upstream origin <new-branch-name>
git push origin --delete <old-branch-name>
```

## Removing an Upstream for a Local Branch

```bash
git branch --unset-upstream <branch-name>
```

## Listing Branches

Examples:

```bash
# local branches
git branch [-l | --list]
# local branches with each last commit
git branch -v
# local branches with each last commit and upstream branch
git branch -vv
# local branches which have merged with current or given branch
git branch --merged [<branch-name>]
# local branches which have NOT merged with current or given branch
git branch --no-merged [<branch-name>]
# branches with/without specific/last commit
git --contains [<commit>]
git --no-contains [<commit>]
# local and remote branches
git branch -a | --all
# remote branches only
git branch -r | --remotes
```

### ... Ordered by Committer Date

```bash
git for-each-ref --sort=-committerdate refs/heads/
# Or using git branch (since version 2.7.0)
git branch --sort=-committerdate  # DESC
git branch --sort=committerdate  # ASC
# or
git for-each-ref --sort=committerdate refs/heads/ --format='%(HEAD) %(color:yellow)%(refname:short)%(color:reset) - %(color:red)%(objectname:short)%(color:reset) - %(contents:subject) - %(authorname) (%(color:green)%(committerdate:relative)%(color:reset))'
# Source: <https://stackoverflow.com/questions/5188320/how-can-i-get-a-list-of-git-branches-ordered-by-most-recent-commit>
```
