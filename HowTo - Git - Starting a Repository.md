# HowTo - Git - Starting a Repository

REF.: [Git Book - 2.1 Git Basics - Getting a Git Repository](http://book.git-scm.com/book/en/v2/Git-Basics-Getting-a-Git-Repository)

----

## Preparations

- Install Git, if you not already have done so.  
    REF.: [Git Book - 1.5 Getting Started - Installing Git](http://book.git-scm.com/book/en/v2/Getting-Started-Installing-Git)
- _Optional (but recommended):_ Create an account for the online repository hoster of your choice.  
    REF.: [Git Book - 4.9 Git on the Server - Third Party Hosted Options
](http://book.git-scm.com/book/en/v2/Git-on-the-Server-Third-Party-Hosted-Options)

## Initializing a Local Directory

1. Create and/or **go to the project directory**.

2. ```bash
   # Make current folder a git repository
   git init
   ```

3. ```bash
   # Add the files you want to track changes
   git add *.py
   git add LICENSE 
   ```

4. ```bash
   git commit -m "Initial commit" 
   ```

## Cloning an Existing Repository

```bash
git clone https://path-to/the-project.git
# or use a different name
git clone https://path-to/the-project.git myVersion
```
