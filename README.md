# GIT-FOUNDATIONS

### WHAT IS VERSION CONTROL ?

- Version Control is a system that records changes to a file or set of files over time so that you can recall specific version later.
- VCS also generally means that if you screw things up or lose files,you can easily recover.

### TYPES OF VERSION CONTROL ?

- Types of VCS :

1. Local Version Control Systems :

   ```
   Local version control systems store all the versions of a project on a local machine. They use a simple database to keep track of changes made to the code.
   Examples: RCS (Revision Control System)
   ```

2. Centralized Version Control Systems:

   ```
   Centralized version control systems store all the versions of a project on a single central server. Clients can check out files from the server, make changes, and then commit those changes back to the server.
   Examples : 
   CVS(Concurrent Versions System)
   SVN (Subversion)
    ```

3. Distributed Version Control Systems :

```
Distributed version control systems allow multiple developers to collaborate on a project by creating local repositories on their machines. Each developer has a full copy of the entire project history, which makes it easier to collaborate and track changes.
Examples: 
Git
Mercurial
Bazaar
```

### WHY IS GIT ?

1. Distributed version control
2. Speed and performance
3. Security and integrity
4. Flexibility and customization
5. Open-source and community-driven
6. Key features of Git:
   - Version control
   - Branching and merging
   - Distributed workflow
   - Security and authentication

### GIT INSTALLATION

1. Download the Git installer from the official Git website.
2. [GIT-Click here](https://git-scm.com/downloads)
3. [GIT-DOCS Click here](https://git-scm.com/docs)
4. [GIT-CheatSheet Click here](https://training.github.com/downloads/github-git-cheat-sheet/)

### GIT SETUP

1. All Configs :-

```
git config --list

```

2. Identity Configs :

```
git config --global user.name "Your Name"
git config --global user.email "your email"
git config --global color.ui auto
git config --global merge.conflictstyle diff3
git config --global credential.helper cache (Do not enter password multiple time)

```

3. Text Editor Config:

```
git config --global core.editor vim

```

### IMPORTANT TERMINOLOGIES

- SCM
- Repository
- Working Directory
- Checkout
- Staging Area
- Commit
- SHA
- Branch

### REPOSITORIES IN GIT

- A software repository is the centralized storage location for software pakages.
- Two types:
   1. Local Repository (user1,user2...)
   2. Remote Repository (centralized Server)

### CREATING REPOSITORIES IN GIT

- Two ways of creating Repository
  
  1. Initializing a Git Repository in Local Machine

    ```
    git init
    ```

    ```
    git status
    ```
  
  2. Cloning a Git Repository from Remote Server (Remote Repository)

    ```
    git clone URL
    ```

### CHECK REPOSITORY HISTORY

- Show all commits
- Checking the logs of repo
- View Modified Files
- View File Changes
- view a specific commit

    ```
    git log
    ```

    ```
    git log --oneline
    ```

    ```
    git log --stat
    ```

    ```
    git log --patch
    ```

    ```
    git show <commit id>
    ```
    ```
    git log --graph --oneline --branches
    ```

### DOING COMMITS

- Git add

   ```
    git add .
    ```

- Git commit
- Commit Messages

    ```
    git commit -m "commit message"
    ```

### GIT DIFF

- git diff is a command in Git that allows you to view the differences between two versions of a file or a set of files. It's a powerful tool for tracking changes and understanding what's been modified in your codebase.
  
  ```
  git diff
  ```

  ```
  git diff --cached
  ```

  ```
  git diff HEAD
  ```

  ```
  git diff <branch-name>
  ```

- View changes before committing
- Compare different versions of a file
- View changes between branches
  
### GIT RESTORE

- git restore is a Git command that allows you to restore the working tree files with the content from a given tree. It's commonly used to discard local changes or to restore files to a previous state.
  
 ```
 git restore --source=<tree> <file name>
 ```

 ```
 git restore --staged <file name>
 ```

 ```
 git restore --worktree <file name>
 ```

 ```
 git restore --patch <file name>
 ```

### GIT IGNORE?

- A .gitignore file is a crucial part of any Git repository, as it specifies intentionally untracked files that Git should ignore. This means that files already tracked by Git are not affected, but any new files matching the patterns in the .git ignore file will not be tracked.
- .gitignore File
- A local .gitignore file is usally placed in the root directory of a project.
  
### TAGGING

- Tagging is an mechnism used to create a snap shot of a Git Repository.
- Tagging is traditionally used to create semantic version number identifier tags that correspond to software release cycles.
  
    ```
    git tag
    ```

- Two types of Tags
  
 1. Annotated Tags (v1.0, v2.0)

   ```
   git tag -a v1.0.1
   ```

 2. Lightweight Tags (1.2.3, 1.2.4)

   ```
   git tag v1.0.2
   ```

   ```
   git tag -d v1.0.1 (delete)
   ```

### BRANCHING

- Branches allow you to work on different parts of a project without impacting the main branch.
- When the work is complete,a branch can be merged with the main project.
- You can even switch between branches and work on different projects without them interfering with each other.

    1. Creating Branches

         ```
         git branch (check branch)
         ```

         ```
         git branch <branch-name>  (create branch)
         ```

    2. Switching Branches

         ```
         git checkout <branch-name>  
         ```
         ```
         git checkout -b dev (create and switch branch)
         ```
         ```
         git switch -c <branch-name>   (Git version 2.23 and above)
         
         ```
    3. Merging Branches
    4. Deleting Branches
   
         ```
         git branch -d <branch-name>
         ```

   
   <b>When to use which command:</b> If you are working with a version of Git that supports the git switch command (Git version 2.23 and above), it's recommended to use git switch for changing branches and git checkout for discarding changes in your working directory.



### MERGING

- Merging takes the contents of a source branch and integrates them with a target branch.
- In merging,only the target branch is changed.The source branch history remains the same.
   1. Fast Forward merge
   2. Regular Merge

   ```
   git log --online --graph --all (check all commit in all branches)
   ```

   ```
   git merge <branch-name>
   ```

### MERGE CONFLICTS

- A merge conflict occurs when two or more files have diverged and cannot be merged into a single file.
- "Merge conflicts" can occur in the process of integrating commits from a different source branch.
- When a merge cannot be fully performed automatically then a merge conflict takes place.
- Git will try to combine as much as it can,but then it will leave special markers (e.g. >>> and <<< )
- `|||` ->  Merged anchestor.
- `===` -> end of the anchestor
-  `>>>` -> incoming change.
- `<<<` -> Current branch
- Change manually on text editor (vs code).

### REMOTE REPOSITORIES

- Remote repositories are versions of your project that are hosted on the internet or network somewhere.
- GITHUB
- BITBUCKET
- GITLAB

### CLONING REPOSITORIES

- Git clone is a Git command line utility which is used to target an existing repository and create a clone,or copy of the target repository.
- Git supports a few network protocols to connect to remote repos line connection strings,ssh links etc.
  
### WORKING WITH REMOTE REPOSITORIES

- List all Remotes
  
  ```
  git remote -v
  ```

- Adding Remotes

  ```
  git remote add <remote-name> <url>
  ```

- Deleting Remotes
  
 ```
 git remote rm <remote-name>
 ```

 ```
 git remote remove <remote-name>
 ```

- Manually edit .git/config file

### PUSHING IN GITHUB

- Git push is a Git command line utility which is used to push changes from your local repository to a remote repository.

    ```
      git push -u <remote-name> <branch-name>
      git push -u origin main
    ```

### PERSONAL ACCESS TOKEN SETUP

- [PAT CLICK HERE](https://docs.github.com/en/authentication/keeping-your-account-and-data-secure/managing-your-personal-access-tokens)

   To create a personal access token in GitHub, follow these steps:

  1. Log into the online administrative console.
  2. Under your GitHub user profile (not the repository profile), click the “Settings” link.
  3. Scroll down and click the “Developer Settings” link.
  4. Click the GitHub “Personal access tokens” link.
  5. Click the “Generate new token” link and provide your password again if required.
  6. Provide a name for the GitHub personal access token in the “Note” field.
  7. Set the access token’s expiration timeout to “No expiration.”
  8. Click the checkbox for every permission scope to give your GitHub token full repository access.
  9. Click “Generate token.”
  10. Copy the GitHub Personal Access Token and use this as the password when you do a Git push to GitHub.
  
  [ REFERENCE CLICK HERE ](https://www.geeksforgeeks.org/how-to-generate-personal-access-token-in-github/)


### PULL REQUESTS?

- Pull requests let you tell others about changes you have pushed to a branch in a repository on GitHub.
- Once a pull request is opend,you can discuss and review the potential changes with collaborators and add follow-up commits before your changes are merged into the base branch.
- A pull request (PR) in GitHub is a proposal to merge changes from one branch to another. Pull requests are useful for collaboration, code reviews, and maintaining a well-documented codebase. 

   1. Go to the repository's main page 
   2. In the Branch menu, select the branch with your commits 
   3. Click Compare & pull request in the yellow banner above the file list 
   4. Select the branch to merge into from the Base branch dropdown menu 
   5. Select the topic branch from the Compare branch dropdown menu 
   6. Enter a title and description for the PR 
   7. Click Create Pull Request to create a PR for review, or Create Draft Pull Request to create a draft PR .


### FETCHING & PULLING

- Git fetch is a command that allows you to download objects from another repository. 
   
   ```
   git fetch <REMOTE-NAME> <BRANCH-NAME>
   ```
     ```
   git merge <REMOTE-NAME> <BRANCH-NAME>
   ```
- Git pull is a command that allows you to fetch from and integrate with  another repository or local branch.
- A git pull is actually a git fetch followed by an additional action(s)
typically a git merge.

   ```
   git pull <REMOTE-NAME> <BRANCH-NAME>
   ```

   * Update the Local form Remote : 
   
    1. fetch :
         - git fetch
         - git merge 
    
    2. pull (fetch + merging)
         - git pull    

[ GIT FETCH & PULL CLICK HERE ](https://docs.github.com/en/get-started/using-git/getting-changes-from-a-remote-repository)

[atlassian Resources  CLICK HERE ](https://www.atlassian.com/git/tutorials/syncing/git-fetch) - Follow this URL.


### FORK

- A fork is a copy of repository. Forking a repository allows you to freely expeiment with changes without affecting the original project.
- Reasons for forking the repository:
   * Propose changes to someone else's project.
   * Use an existing project as a starting point.

 [FORK CLICK HERE](https://www.freecodecamp.org/news/how-to-fork-a-github-repository/) 

 [FORK GITHUB CLICK HERE ](https://docs.github.com/en/pull-requests/collaborating-with-pull-requests/working-with-forks/fork-a-repo)


### REBASHING 

- Rebasing is the process of taking one branch and adding it to tip of another,where the tip is simply the last commit in the branch.
- Rebasing changes the history of your branch.
- Merge = Adding the commits together with master branch.
  
  ```
  git rebase <branch-name> 
  ```
  [REBASHING CLICK HERE](https://www.atlassian.com/git/tutorials/rewriting-history/git-rebase)

### INTERACTIVE REBASHING

- Interactive Rebasing changes the history of your branch.
- Different Options available: 
    * Squash
    * Amend
    * Reword
    * Delete
    * Reorder
    * Split 
    * Fixup

   ```
   git rebase --interactive HEAD~7 (top 7 commit merge)
   git rebase --i  HEAD~7
   ```

[ INTERACTIVE REBASHING CLICK HERE](https://docs.github.com/en/get-started/using-git/about-git-rebase)


### CHERRY PICKING IN GIT

- Cherry-picking in Git stands for applying some commit from one branch into another branch.
- When we do cherry picking
   * Bring in changes from specific commit
   * Choose one or commits 

      ```
      switch master branch
      git cherry-pick <sha-id of other branch commit>
      ```

[CHERRY PICK CLICK HERE ](https://www.atlassian.com/git/tutorials/cherry-pick) 


### MODIFY RECENT COMMITS

- Git provides you the option to amend the last commit using.
  
  ```
  git commit --amend
  git commit --amend -m "<commit message>"
  ```
- Modifying the last commit 
  
   * Helps in editing the commit message
   * You can add forgotten files in the last commit.

### REVERT COMMIT

- Git revert undoes the changes made by a previous commit by creating an entirely new commit all without altering the history of commits.
- If a character is added in commit A,if Git reverts commit A,then Git will make a new commit where that charcter is deleted. 

   ```
   git revert <commit-id>
   ```

### GIT CHECKOUT COMMIT

- Git checkout commited means that you take any given commit from the repository and re-create the state of the associated file and directory tree.
- You can also switch branches
- You can also create and switch a branch instantly.

[GIT CHECKOUT COMMIT CLICK HERE ](https://git-scm.com/docs/git-checkout)

   ```
   git checkout <commit-id>
   ```

### GIT RESET 

- The git reset command is used to reset the changes.
- It allows you to shape history or crafting commits.
- 3 different modes :

   * Soft: used to unstage the files which we have staged using the git add command.  
   ```
       git reset --soft HEAD~3
   ``` 
   *  Mixed: used to remove the file which we have commited using the git commit command.
   * Hard: used to remove all things which we have placed in our code.

   ```
      git reset <mode> <sha-id/commit-id>
   ```
    [GIT RESET CLICK HERE ](https://git-scm.com/docs/git-reset) 

### STASHING

- Stashing saves a copy of your uncommitted changes.i.e working area and staging area in a queue,off to the side of your project.

  ```
  git stash
  ``` 

  [STASHING CLICK HERE ](https://git-scm.com/docs/git-stash)

- Retrieve on woking directory, 2 methods:
   1. Apply
   2. pop

### REFLOG

- Reflog is a mechanism to record the changes in branches and save the history.
- This command is to manage the information recorded in all branches.
- Every action you perform inside of Git where data is stored,you can find it insude of the reflog.

   ```
   git reflog
   ```
   ```
   gitk   (for graphically)
   gitk --all
   ```

   ```
   git config gc.reflogexpireunreachble 30
   ``` 
   ```
   git reset --hard <commit-id>
   ```
   ```
   cd .git/logs/
   ls
   cd refs/
   ls
   cd heads/
   ls (master,feture,code...)
   vi master (start to end changes show)
   ```

  [ REFLOG CLICK HERE ](https://www.atlassian.com/git/tutorials/rewriting-history/git-reflog)