# Git: Key Concepts, Commands, and Workflow

> Contributors:  
> - Maksym Borsuk  
> - Didusenko Oleksandr

>this part is made by Maksym Borsuk 

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

>this part made by Didusenko Oleksandr

---

A **"commit"** is the process of saving changes in a version control system like Git. When you make a commit, you're essentially taking a "snapshot" of the current state of your project and recording it in the project's history. This allows you to track and review all changes made over time.

### How do commits help track changes?
1. **Saving the project's state**: Each commit saves a specific version of the files along with a description of the changes made (the commit message). This makes it easier to understand what was changed and why.

2. **History of changes**: Commits create a chronological log of all changes in the project. Using commands like `git log`, you can see who made changes, when, and what was modified.

3. **Reverting to previous versions**: If something goes wrong, commits allow you to go back to a previous version of the project by selecting a specific commit.

4. **Collaboration**: In team projects, commits allow developers to see which parts of the project were modified by others.

5. **Identifying changes**: Each commit has a unique identifier (a hash), which makes it easy to reference a specific change in the project's history.

### How to create a commit in Git?
1. **Stage the files (add them to the staging area)**:
   ```
   git add <file_name>   # Add a specific file
   git add .             # Add all changed files
   ```

2. **Create the commit**:
   ```
   git commit -m "Description of the changes"
   ```

   The description should be clear and informative, e.g., `"Added login functionality"` or `"Fixed a bug in the display function"`.

### Why are commits important?
- **Structure**: Commits help keep the project organized by documenting every change made, which makes it easier to understand the code, even after a long time.
- **Data Safety**: Commits reduce the risk of losing work since the change history is always accessible.
- **Teamwork**: In collaborative environments, commits make it easy to keep track of who made what changes.

