# GitHub - Renaming a Repository

REF.: [1] [GitHub Docs - Renaming a repository](https://docs.github.com/en/repositories/creating-and-managing-repositories/renaming-a-repository)  
REF.: [2] [Stack Overflow - Github: What happens to forks when a repository is renamed?](https://stackoverflow.com/questions/57984409/github-what-happens-to-forks-when-a-repository-is-renamed#:~:text=Forks%20don't%20get%20renamed,relationship%20with%20the%20parent%20repo.)

**Note:**

- "When you rename a repository, all existing information, with the exception of project site URLs, is automatically redirected to the new name, [...]" [1]
- "All git [...] operations targeting the previous location will continue to function as if made on the new location." [1]
- "Forks don’t get renamed, but maintain their relationship with the parent repo. Watches and stars are preserved." [2]

**Warning:** ⚠️

- Make sure that your repository isn't linked to `other services` before renaming. It's not everywhere supported. Remember to update changes there as well if possible and necessary.
- If your repository has a `GitHub Pages` site, the site's URL _**will be impacted**_ by renaming the repository.

----

## Renaming a Repository

1. Log-in to GitHub and open the repository's `Settings`.

2. Under `General` go to the repository name and enter a new one.

3. _(Optional, but recommended)_  
   Update your local clones to point to the repository's new URL.

```bash
git remote set-url origin NEW_URL
```
