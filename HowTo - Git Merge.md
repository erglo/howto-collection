# HowTo - Git Merge

REF.: [Git - git-merge Documentation](https://git-scm.com/docs/git-merge)  

----

## Merging an other Branch to the `main` Branch

```bash
# Current branch is "main"
git merge <feature_branch>
```

----

## Dealing with Merging Conflicts

A graphical tool to resolve merging issues:

```bash
git mergetool
```

**Hint:** See ["HowTo - Git and VS Code.md"](./HowTo%20-%20Git%20and%20VS%20Code.md) to learn how to set VS Code as your default merge tool.

## Cancel Merging After a Conflict

```bash
git merge --abort
```
