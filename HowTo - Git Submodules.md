# HowTo - Git Submodules

REF.: [Git Submodules basic explanation](https://gist.github.com/gitaarik/8735255)  
REF.: [Git submodules best practices
](https://gist.github.com/slavafomin/08670ec0c0e75b500edbaa5d43a5c93c)

----

**Note:** The submodule is just a separate repository.  
**Note:** Don't forget to commit changes!

## Adding a submodule

```shell
# Links the submodule with folder "dir_name"
git submodule add git@github.com:name/repo.git [dir_name] 
```

## Getting the submodule's code

```shell
git submodule update [--init] [--recursive]
```

## Clone a repository with submodules

```shell
git clone --recursive git@github.com:name/repo.git
```

## Useful configuration settings

```shell
# Add status of submodules to `git status`
git config --global status.submoduleSummary true
```

```shell
# W/o config setting 
git diff --submodule=log
# See submodule changes with `git diff`
git config --global diff.submodule log
```

```shell
# Check if already set to "on-demand"
git config --global fetch.recurseSubmodules 
```

## Updating a submodule

```shell
# Get all new data from the remote to local cache 
cd dir_name  # submodule folder in your repo
git fetch
# Log to verify what you have 
git log
# Checkout on the desired checksum
git checkout -q <ckecksum>
cd ..  # back to your repo
```

## Removing a submodule

```shell
# Remove permanently 
git rm dir_name 
# This will update the `.gitmodules` file as well 
```

```shell
# Unregister but keep reference in `. gitmodules` file 
git submodule deinit
# Remove remaining empty local submodule folder (w/o `git`) 
rm dir_name 
```
