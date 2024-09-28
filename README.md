# GIT-FOUNDATIONS

### WHAT IS VERSION CONTROL ?


 - Version Control is a system that records changes to a file or set of files over time so that you can recall specific version later.
 - VCS also generally means that if you screw things up or lose files,you can easily recover.

### TYPES OF VERSION CONTROL ?

* Types of VCS :

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

### REPOSITORIES IN GIT:

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
   
 * View changes before committing
 * Compare different versions of a file
 * View changes between branches
  
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
   git tag -d v1.0.1 
   ```
### BRANCHING