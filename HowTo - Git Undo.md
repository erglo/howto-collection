# HowTo - Git Undo

REF.: [Git - git-reset Documentation](https://git-scm.com/docs/git-reset)  
REF.: [Git - git-commit Documentation](https://git-scm.com/docs/git-commit)  

**Note:** `Undo` is NOT a git command! It is just referring to help undoing things while using `git`.

----

## Undo Last Commit

```bash
git reset --soft HEAD^
```

## Undo Until Specific Commit

```bash
git reset --soft <hash>
```

_Note: `HEAD^` goes 1 step back, `HEAD^^/HEAD~2` goes 2 steps back, etc._

## Delete Last Commit

```bash
git reset --hard HEAD^
```

## Add Files to Last Commit

```bash
git commit --amend
```
