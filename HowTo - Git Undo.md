# HowTo - Git Undo

### Undo Last Commit

```git
git reset --soft HEAD^
```

_Note: `HEAD^` goes 1 step back, `HEAD^^/HEAD~2` goes 2 steps back, etc._

### Delete Last Commit

```git
git reset --hard HEAD^
```

### Add Files to Last Commit

```git
git commit --amend
```
