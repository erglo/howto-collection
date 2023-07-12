# GitHub - Contributing to a Project

REF.: [Git Book - 6.2 GitHub - Contributing to a Project](http://book.git-scm.com/book/en/v2/GitHub-Contributing-to-a-Project)

----

## The GitHub Flow

1. Fork the project.

2. Create a new branch from `main` with a descriptive name, starting eventually with an issue number.

3. Make some changes and commit them to improve the project.

4. Push this branch to your GitHub project.

5. Open a Pull Request on GitHub.

6. Discuss, and optionally continue committing.

7. The project owner merges or closes the Pull Request.

8. Sync the updated `main` back to your fork.

## The Local Flow

1. Clone a fork of the project locally.

    ```bash
    git clone https://path-to/the-project.git
    ```

2. Create a descriptive topic branch and switch to it.

    ```bash
    git checkout -b <new-feature>
    # or 
    git switch -c <new-feature>
    ```

3. Make your change to the code.

4. Check that the change is good.

5. Add and commit the change to the topic branch.  
   (**Note:** Use _imperative present tense_ for commit messages.)

    ```bash
    git add .
    git commit -m 'Change XYZ'
    # or
    git commit -a -m 'Change XYZ'
    # or
    git commit -am 'Change XYZ'
    ```

6. Push your new topic branch back up to your remote fork.

    ```bash
    git push origin <name-of-branch>
    ```

7. Continue from step `5` in the [The GitHub Flow](#the-github-flow) above.
