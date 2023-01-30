# HowTo - Git - Starting a Repository

:link: [Git Book - 2.1 Git Basics - Getting a Git Repository ](http://book.git-scm.com/book/en/v2/Git-Basics-Getting-a-Git-Repository)

----

### Preparations

- Install Git if you not already have done so.  
    :link: [Git Book - 1.5 Getting Started - Installing Git](http://book.git-scm.com/book/en/v2/Getting-Started-Installing-Git)
- _Optional (but recommended):_ Create an account for the online repository hoster of your choice.  
    :link: [Git Book - 4.9 Git on the Server - Third Party Hosted Options
](http://book.git-scm.com/book/en/v2/Git-on-the-Server-Third-Party-Hosted-Options)

### Initializing a Local Directory

1. Create and/or **go to the project directory**. 

2. ```git 
    git init
    ```

3. ```git
    git add *.py
    git add LICENSE 
    ```

4. ```git
    git commit 'Initial project version' 
    ```

### Cloning an Existing Repository

```git
git clone https://path-to/the-project.git
```

_or_

```git
git clone https://path-to/the-project.git myVersion
```
