# HowTo - Git Submodule

REF.: [Git Submodules basic explanation](https://gist.github.com/gitaarik/8735255)  
REF.: [Git submodules best practices
](https://gist.github.com/slavafomin/08670ec0c0e75b500edbaa5d43a5c93c)  

**Note:**

- The submodule is (just) a separate repository.
- Don't forget to commit changes!

----

## Adding a submodule

```bash
# Links the submodule with folder "dir_name";
# if you don't set a dirname the repo's name will be used instead
git submodule add https://path-to/the-submoule-repo.git [dir_name] 
git commit -m "Add submodule <name>"
```

## Updating the submodule's code

```bash
git submodule update [--init] [--recursive]
```

## Cloning a repository with submodules

```bash
git clone --recursive git@github.com:name/repo.git
```

## Useful configuration settings

```bash
# Add status of submodules to `git status`
git config --global status.submoduleSummary true
```

```bash
# W/o config setting 
git diff --submodule=log
# See submodule changes with `git diff`
git config --global diff.submodule log
```

```bash
# Check if already set to "on-demand"
git config --global fetch.recurseSubmodules 
```

## Updating a submodule

```bash
# Get all new data from the remote to your local cache 
cd dir_name  # submodule folder in your repo
git fetch
# Log to verify what you have 
git log
# Checkout on the desired checksum
git checkout -q <ckecksum>
# or use 'git pull' to get latest submodule changes
cd ..  # go back to your repo
```

## Removing a submodule

```bash
# Remove permanently 
git rm dir_name 
# This will update the `.gitmodules` file as well 
```

```bash
# Unregister but keep reference in `. gitmodules` file 
git submodule deinit
# Remove remaining empty local submodule folder (w/o using `git`) 
rm dir_name 
```
