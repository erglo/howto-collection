# HowTo - Git Stash

> REF.: [Git - git-stash Documentation](https://git-scm.com/docs/git-stash)  
> REF.: [How to Apply Git Stash to a Different Branch?](https://www.designcise.com/web/tutorial/how-to-apply-git-stash-to-a-different-branch) by _Daniyal Hamid_  
> REF.: [Git - git-rebase Documentation](https://git-scm.com/docs/git-rebase)
----

## Saving Changes to a Stash

```bash
git stash
# or
git stash save  # deprecated, use 'push' instead
# or
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
git stash pop    # loads top hash, stash@{0} and removes it
# or
git stash apply  # like 'pop' but without removing the entry
```

## Removing an Entry from the Stash

```bash
git stash pop             # loads top hash, stash@{0} and removes it
# or
git stash drop            # drop top hash, stash@{0}
# or
git stash drop stash@{n}  # drop specific stash - see 'git stash list'
```

## Removing all Entries from the Stash

```bash
git stash clear
```

## Using an Entry in a Different Branch

```bash
git stash                   # save current changes
git switch <other_branch>   # change branch; same as 'git checkout'
git stash pop               # use top entry, stash@{0}
```

## Creating a new Branch from the Stash

```bash
git stash                       # save current changes
git stash branch <new_branch>   # use top entry and create new branch
```

## Comparing Changes from Stash to Current Branch

```bash
git stash show -p               # see most recent entry
git stash show -p stash@{n}     # see stash entry number <n>
```

## Adding Previous Commit to Stash

```bash
# If not already pushed to remote repository do this...
git rebase -i HEAD~2
# This will open your default editor.
# Now reorder the two commits (they are listed oldest => newest) from this...
> pick 222 commit to be stashed
> pick 111 commit to be pushed to remote
# to this...
> pick 111 commit to be pushed to remote
> pick 222 commit to be stashed
# Save + exit and wait for git to finish. Now you can ...
git reset --soft HEAD~1
git stash
# Source: <https://stackoverflow.com/questions/26884364/how-to-stash-my-previous-commit>
```
