# GitHub - Rename a repository

1. Log-in to GitHub and open the repository's `Settings`.

2. Go to the repository name and enter a new one.

3. Update your local clones to point to the repository's new URL.

```bash
$ git remote set-url origin NEW_URL
```

**Note:** _"All git [...] operations targeting the previous location will continue to function as if made on the new location."_

Source: [GitHub Docs - Renaming a repository](https://docs.github.com/en/repositories/creating-and-managing-repositories/renaming-a-repository)
