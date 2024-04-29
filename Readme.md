## Amending commits

### What is amending?
* It lets you combine staged changes with the previous commit instead of creating an entirely new commit.
* It can also be used to simply edit the previous commit message without changing its snapshot.
* But, amending does not just alter the most recent commit, it replaces it entirely, meaning the amended commit will be a new entity with its own ref. 

## Rewording commit messages  
* this is used to change the git commit messages 
* Steps to do so
    * step1 : select the commits to interact with
    ```bash
        # to interact with 2 commits
        git rebase -i HEAD~2
    ```
    * Step2 : this will open the vim editor to choose options to apply on independent commits
    ```bash
        # choosing reword option
        reword <commit-id>
    ```
    * Step3 : save and quit
    * Step4 : check git log to confirm if git commit message has been changed or not
    ```bash
        git log --oneline
    ```

## Deleting commits
* this command is used to drop/delete a git commit
* Steps to do so
    * Step 1: select the number of commits to interact with using git rebase
    ```bash
        # to interact with 2 commits
        git rebase -i HEAD~2
    ```

    * Step 2: change the option to drop in front of the commit hash, which you want to delete
    ```bash
        # droping commit id
        drop <commit-hash>
    ```

    * Step 3: Save and quit
    * Step 4: check the git log to see the change
    ```bash
        git log --oneline
    ```

## Reordering commits
* we can change order of the git commit history
* Steps to do so:
    * Step 1: select the number of commits to interact with using git rebase
    ```bash
        # to interact with 2 commits
        git rebase -i HEAD~2
    ```
    * Step 2: order the commit as per the requirement.
    * Step 3: save and exit
    * Step 4: check the git log to see the change
    ```bash
        git log --oneline
    ```


## Squashing commits 
* This command is used to merge different commits into one commit
* Steps to sqash a commit:
    * Step 1: select the number of commits to interact with using git rebase
    ```bash
        # to interact with 2 commits
        git rebase -i HEAD~2
    ```
    * Step 2: select the commit which we want to merge, and change the keyword from pick to fixup/squash
    * Step 3: save and exit
    * Step 4: check the git log to see the change
    ```bash
        git log --oneline
    ```
### Squash vs Fixup 
* Squash will give option to edit the commit messages.
* Fixup will discard the git message which will be going to merge in to different repository


## Splitting commits 

## How to make a GIT repo

### Method 1 (create Remote repository then clone to local repository)
    * login into the github account
    * create new repo with readme.md file
    * clone repository on the local machine

### Method 2 (Create Local repository then map to Remote repository)
    * create a local folder 
    * intialise this folder as git repository using git init
    * now make a local commit on this repository
    * map the remote repository to this local drive 
    * push the changes to remote repository

 
