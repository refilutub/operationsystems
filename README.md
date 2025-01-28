# Git: Key Concepts, Commands, and Workflow

> Contributors:  
> - Maksym Borsuk  
> - Didusenko Oleksandr

>this part is made by refilutub

Git is a **distributed version control system (DVCS)** used to track changes in source code during software development. It enables multiple developers to collaborate on a project, manage different versions of code, and maintain a complete history of changes.

---

## What is Git Used For?

- **Version Control**: Track changes to files over time.
- **Collaboration**: Allow multiple developers to work on the same project simultaneously.
- **Branching and Merging**: Create separate branches for features or fixes and merge them back into the main codebase.
- **Backup and Restore**: Maintain a complete history of the project, allowing you to revert to previous versions if needed.
- **Code Review**: Facilitate code reviews through pull requests (PRs) and merge requests (MRs).

---

## Key Git Actions and Commands

### 1. **Initialize a Repository**
   - Create a new Git repository:
     ```bash
     git init
     ```

### 2. **Clone a Repository**
   - Clone an existing repository:
     ```bash
     git clone <repository_url>
     ```

### 3. **Stage Changes**
   - Add files to the staging area:
     ```bash
     git add <file_name>
     ```
   - Add all changes:
     ```bash
     git add .
     ```

### 4. **Commit Changes**
   - Commit staged changes with a message:
     ```bash
     git commit -m "Your commit message"
     ```

### 5. **Check Status**
   - View the status of your working directory:
     ```bash
     git status
     ```

### 6. **View Commit History**
   - View the commit history:
     ```bash
     git log
     ```

### 7. **Branching**
   - Create a new branch:
     ```bash
     git branch <branch_name>
     ```
   - Switch to a branch:
     ```bash
     git checkout <branch_name>
     ```
   - Create and switch to a new branch:
     ```bash
     git checkout -b <branch_name>
     ```

### 8. **Merging**
   - Merge a branch into the current branch:
     ```bash
     git merge <branch_name>
     ```

### 9. **Pull Updates**
   - Fetch and merge changes from a remote repository:
     ```bash
     git pull
     ```

### 10. **Push Changes**
   - Push local changes to a remote repository:
     ```bash
     git push
     ```

### 11. **Revert Changes**
   - Undo changes in a file:
     ```bash
     git checkout -- <file_name>
     ```
   - Revert a commit:
     ```bash
     git revert <commit_hash>
     ```

### 12. **Stashing**
   - Temporarily save changes without committing:
     ```bash
     git stash
     ```
   - Apply stashed changes:
     ```bash
     git stash apply
     ```

### 13. **Tagging**
   - Create a tag for a specific commit (e.g., for releases):
     ```bash
     git tag <tag_name>
     ```

### 14. **Remote Management**
   - Add a remote repository:
     ```bash
     git remote add <remote_name> <repository_url>
     ```
   - View remote repositories:
     ```bash
     git remote -v
     ```

---

## Key Git Terms

- **Repository (Repo)**: A directory where Git tracks changes to files.
- **Commit**: A snapshot of changes saved in the repository.
- **Branch**: A separate line of development, allowing work on features or fixes without affecting the main codebase.
- **Merge**: Combining changes from one branch into another.
- **Clone**: Creating a local copy of a remote repository.
- **Pull**: Fetching changes from a remote repository and merging them into the local branch.
- **Push**: Uploading local changes to a remote repository.
- **Staging Area**: A place where changes are prepared before committing.
- **HEAD**: A reference to the current commit or branch.
- **Tag**: A marker for a specific point in the commit history (e.g., for releases).
- **Stash**: Temporarily saving changes without committing them.
- **Remote**: A connection to a remote repository (e.g., on GitHub or GitLab).
- **Conflict**: A situation where Git cannot automatically merge changes, requiring manual resolution.
- **Pull Request (PR) / Merge Request (MR)**: A request to merge changes from one branch into another, often used for code review.

