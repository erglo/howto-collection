# HowTo - Using Tags with Git

REF.: [Git Book - 2.6 Git Basics - Tagging](http://book.git-scm.com/book/en/v2/Git-Basics-Tagging)

----

## Adding a New Tag

```bash
git tag <tagname>
```

## Deleting a Tag

```bash
git tag -d <tagname>
```

## Renaming a Tag

```bash
git tag <new_tagname> <old_tagname>
```

### Renaming a Remote Tag

```bash
git push origin <new_tagname> :<old_tagname>
```

**Note:** The colon `:` removes the tag from the remote repository. Everyone else needs to update locally as well with `git pull --prune --tags`.

## Listing Tags

```bash
git tag [--list or -l]
# or list with optional string pattern
git tag -l <pattern>
# or list with commit message
git tag -n
```

## Tagging Later

```bash
# Tag a specific commit hash
git tag -a <tagname> 9fceb02
```

## Sharing Tags Remotely

```bash
git push origin <tagname>
# or sharing all tags at once
git push origin --tags
# not recommended; this might trigger unwanted actions (!)
```

## Deleting a Remote Tag

```bash
git push origin --delete <tagname>
```
