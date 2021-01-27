# github-flow

### Step by step basic github flow
- Clone the repository and enter the directory where the repository is located.

    ```
    git clone git@github.com:mayurva/github-flow.git
    cd github-flow
    ```

- Find the default branch of the repository. Traditionally, the default branch is ```master```, but new repos would have ```main``` as the default branch.

    ```
    $ git branch
    * main
    ```

- Create a feature branch

    ```
    git checkout -b feature-name
    ```

- Make some changes by adding or modifying a file. For testing, simply update the README file. You can do this using ```vi``` or another editor of your choice.

- View the changes you made

    ```
    git status
    git diff
    ```

- If the changes look good, you can commit them locally.

    ```
    git add .
    git commit -m "Meaningful commit message"
    ```

    Note: Commits are a unit of change. Your task may be simple enough to be covered in a single commit, or it may require multiple commits. You can make more changes and create a new commit by following the above steps. If your commit is complicated enough to require multiline commit message, you can simply run the following command. It is recommended to provide as much information in the commit message so that the person reviewing your commit has full context.

    ```
    git commit
    ```

- Once you finish commiting the change, it is good practice to rebase your changes with the default branch (master or main). This way your branch will be up to date with the default branch.

    ```
    git checkout <default-branch>
    git pull
    git checkout feature-name
    git rebase <default-branch>
    ```

- Push your branch upstream.

    ```
    git push -u origin feature-name
    ```

    For subsequent pushes you can simply run ```git push```.

- Create a pull request from the Github Web UI. When you push to a branch for the first time, the ```git push``` command provides a link to create a pull request.

- If you get any review comments, address them and commit again. Once you push this change upstream, your pull request will automatically get updated.

- Once your pull request is approved, merge it in the Github web UI.

### Advanced topic

##### Force pushes

##### Rebase vs Merge

##### Squashing commits
