# HowTo - Git Bash - Using `alias` on Windows

REF.: [Dev.to - Git Bash on Windows: adding a permanent alias](https://dev.to/mhjaafar/git-bash-on-windows-adding-a-permanent-alias-198g) by Hafiz Jaafar

----

## Checking Available Aliases

```bash
$ alias
# alias ll='ls -l'
# alias ls='ls -F --color=auto --show-control-chars'
```

## Adding a Permanent Alias

```bash
$ explorer C:/Program\ Files/Git/etc/profile.d/
# Edith `aliases.sh` in administrator mode
```

**Note:**  

- Sometimes the Git folder is in the local user's `AppData` directory:  
  `/c/Users/<username>/AppData/Local/Programs/Git/etc/profile.d/"`
- Do _not_ use any whitespace characters directly before or after the equal sign (=).
