# HowTo - Git Stash

REF.: [Git - git-stash Documentation](https://git-scm.com/docs/git-stash)
<!-- https://stackoverflow.com/questions/5737002/how-to-delete-a-stash-created-with-git-stash-create -->
REF.: [How to Apply Git Stash to a Different Branch?](https://www.designcise.com/web/tutorial/how-to-apply-git-stash-to-a-different-branch) by _Daniyal Hamid_

----

## Saving Changes to a Stash

```bash
git stash
# or
git stash save  # deprecated, use 'push' instead
git stash push
# or with optional message
git stash push <message_or_name>
```

## Listing Stash Entries

```bash
git stash list
```

## Loading an Entry from the Stash

```bash
git stash pop    # loads top hash, stash@{0}
git stash apply  # like 'pop' but without removing the entry
```

## Removing an Entry from the Stash

```bash
git stash drop            # drop top hash, stash@{0}
git stash drop stash@{n}  # drop specific stash - see 'git stash list'
```

## Removing All Entries from the Stash

```bash
git stash clear
```

----

## Using an Entry in a Different Branch

```bash
git stash                   # save current changes
git switch <other_branch>   # same as 'git checkout'
git stash pop               # use top entry, stash@{0}
```

## Creating a new Branch from the Stash

```bash
git stash                       # save current changes
git stash branch <new_branch>   # use top entry, stash@{0}
```

## Comparing Changes from Stash to Current Branch

```bash
git stash show -p               # see most recent entry
git stash show -p stash@{n}     # see stash entry number <n>
```
