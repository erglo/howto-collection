# HowTo - Tagging

:link: [Git Book - 2.6 Git Basics - Tagging](http://book.git-scm.com/book/en/v2/Git-Basics-Tagging) 

----

## Lightweight Tags 

### Adding a New Tag

```git
git tag <tagname>
```

### Deleting a Tag

```git
git tag -d <tagname>
```

### Renaming a Tag

```git
git tag <new_tagname> <old_tagname>
git tag -d <old_tagname>
git push origin <new_tagname> :<old_tagname>
```

_Note:_ The **colon** removes the tag from the remote repository. Everyone else needs to update locally as well with `git pull --prune --tags`. 

### List Tags

```git
git tag [--list or -l] 
```

_or_ (with commit message)


```git
git tag -n
```

### Tagging Later

```git
git tag -a <tagname> 9fceb02
```

### Sharing Tags

```git
git push origin <tagname>
```

_or_ (all tags)


```git
git push origin --tags
```

### Deleting a Shared Tag

```git
git push origin --delete <tagname>
```
