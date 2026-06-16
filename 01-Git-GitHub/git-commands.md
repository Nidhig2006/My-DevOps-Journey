# Git Commands Cheat Sheet

A comprehensive collection of commonly used Git commands, workflows, and concepts with explanations and examples.

---

# Table of Contents

* Git Workflow
* Git Stages
* Git Configuration
* Repository Initialization
* Repository Status and History
* Staging Changes
* Committing Changes
* Remote Repository Operations
* Branch Management
* Merge and Rebase
* Git Reset
* Git Stash
* Git Cherry-pick
* Git Tags
* Git Diff
* Undoing Changes
* Cleaning Repository
* Git Aliases
* Common Git Errors
* Working with GitHub
* Daily Git Workflow

---

## Git Workflow

```text
Working Directory
        │
        ▼
    git add
        │
        ▼
  Staging Area
        │
        ▼
   git commit
        │
        ▼
 Local Repository
        │
        ▼
    git push
        │
        ▼
GitHub Repository
```

![Git Workflow](Git%20Basic%20Commands%20%281%29.png)

The above diagram illustrates the standard Git workflow from modifying files to pushing changes to GitHub.

---

## Git Stages

![Git Stages](Git%20Stages%20%281%29.png)

Git manages files through three primary stages:

### Working Directory

The area where you create and modify project files.

### Staging Area (Index)

The temporary area where files are prepared for the next commit using the `git add` command.

### Local Repository

The local database where committed snapshots are permanently stored.

---

## Git Configuration

### Configure Username

```bash
git config --global user.name "Your Name"
```

### Configure Email

```bash
git config --global user.email "your-email@example.com"
```

### View Git Configuration

```bash
git config --list
```

### Set Default Branch Name

```bash
git config --global init.defaultBranch main
```

---

## Repository Initialization

### Initialize a New Repository

```bash
git init
```

### Clone an Existing Repository

```bash
git clone <repository-url>
```

Example:

```bash
git clone https://github.com/username/my-devops-journey.git
```

---

## Repository Status and History

### Check Repository Status

```bash
git status
```

### View Commit History

```bash
git log
```

### View Commit History in One Line

```bash
git log --oneline
```

### View Commit History as a Graph

```bash
git log --graph --oneline --decorate --all
```

### View HEAD History

```bash
git reflog
```

---

## Staging Changes

### Add a Specific File

```bash
git add filename
```

### Add All Files

```bash
git add .
```

### Add All Changes

```bash
git add -A
```

### Unstage a File

```bash
git restore --staged filename
```

---

## Committing Changes

### Create a Commit

```bash
git commit -m "Commit message"
```

### Commit Tracked Files Directly

```bash
git commit -am "Updated project"
```

### Modify the Last Commit

```bash
git commit --amend
```

---

## Remote Repository Operations

### Add a Remote Repository

```bash
git remote add origin <repository-url>
```

### View Remote Repositories

```bash
git remote -v
```

### Change the Remote URL

```bash
git remote set-url origin <new-url>
```

### Remove a Remote Repository

```bash
git remote remove origin
```

### Push Changes

```bash
git push origin main
```

### Push and Set Upstream Branch

```bash
git push -u origin main
```

### Pull Latest Changes

```bash
git pull origin main
```

### Fetch Latest Changes

```bash
git fetch origin
```

---

## Branch Management

![Git Branches](Git%20Branches%20%281%29.png)

### List Local Branches

```bash
git branch
```

### List All Branches

```bash
git branch -a
```

### List Remote Branches

```bash
git branch -r
```

### Create a New Branch

```bash
git branch feature-branch
```

### Switch to a Branch

```bash
git checkout feature-branch
```

or

```bash
git switch feature-branch
```

### Create and Switch to a New Branch

```bash
git checkout -b feature-branch
```

or

```bash
git switch -c feature-branch
```

### Rename the Current Branch

```bash
git branch -m new-branch-name
```

### Delete a Local Branch

```bash
git branch -d branch-name
```

### Force Delete a Branch

```bash
git branch -D branch-name
```

---

## Merge and Rebase

![Git Merge vs Git Rebase](GIt%20Merge%20vs%20Git%20Rebase%20%281%29.png)

| Git Merge                     | Git Rebase                           |
| ----------------------------- | ------------------------------------ |
| Creates a merge commit.       | Rewrites commit history.             |
| Preserves branch history.     | Creates a linear history.            |
| Suitable for shared branches. | Suitable for local feature branches. |

### Merge a Branch

```bash
git merge branch-name
```

### Rebase Current Branch

```bash
git rebase main
```

### Interactive Rebase

```bash
git rebase -i HEAD~3
```

### Continue Rebase

```bash
git rebase --continue
```

### Abort Rebase

```bash
git rebase --abort
```

---

## Git Reset

`git reset` moves the current `HEAD` pointer to a specified commit. Depending on the option (`--soft`, `--mixed`, or `--hard`), it also affects the **staging area** and **working directory** differently.

| Reset Type | Commits | Staging Area | Working Directory |
|------------|----------|--------------|------------------|
| `--soft`   | Removed | Kept | Kept |
| `--mixed`  | Removed | Cleared | Kept |
| `--hard`   | Removed | Cleared | Cleared |

---

### Soft Reset

```bash
git reset --soft HEAD~1
```

**What it does:**
- Moves `HEAD` back by one commit.
- Removes the last commit from the commit history.
- **Keeps all changes staged** (ready to commit again).
- Does **not** modify your working files.

**Use case:**  
When you want to undo the last commit but keep all changes ready for recommitting.

**Before:**
```text
A --- B --- C (HEAD)
```

**After:**
```text
A --- B (HEAD)
         ↑
    Changes from C are still staged.
```

---

### Mixed Reset (Default)

```bash
git reset --mixed HEAD~1
```

or simply

```bash
git reset HEAD~1
```

**What it does:**
- Moves `HEAD` back by one commit.
- Removes the last commit from history.
- **Unstages all changes**, but keeps them in your working directory.
- Your files remain exactly as they were.

**Use case:**  
When you want to undo a commit and review or modify the changes before staging and committing them again.

**Before:**
```text
A --- B --- C (HEAD)
```

**After:**
```text
A --- B (HEAD)
         ↑
 Changes from C are kept as unstaged files.
```

---

### Hard Reset

```bash
git reset --hard HEAD~1
```

**What it does:**
- Moves `HEAD` back by one commit.
- Removes the last commit from history.
- Clears the staging area.
- **Deletes all local file changes related to that commit.**

⚠️ **Warning:** This operation permanently discards uncommitted changes. Use it carefully.

**Use case:**  
When you want to completely throw away the last commit and all associated local changes.

**Before:**
```text
A --- B --- C (HEAD)
```

**After:**
```text
A --- B (HEAD)
```

All changes introduced by commit `C` are removed from both the repository and your working directory.

---

### Quick Comparison

| Feature | `--soft` | `--mixed` | `--hard` |
|----------|-----------|------------|-----------|
| Moves `HEAD` | ✅ | ✅ | ✅ |
| Removes commit | ✅ | ✅ | ✅ |
| Keeps changes in working directory | ✅ | ✅ | ❌ |
| Keeps changes staged | ✅ | ❌ | ❌ |
| Safe for beginners | ✅ | ✅ | ⚠️ Use carefully |

### Memory Trick

- **Soft Reset** → "Undo commit, keep everything staged."
- **Mixed Reset** → "Undo commit, keep files, unstage them."
- **Hard Reset** → "Undo commit and delete everything."

---

## Git Stash

![Git Stash](Git%20Stash%20%281%29.png)

### Save Current Changes

```bash
git stash
```

### Save Changes with a Message

```bash
git stash push -m "Work in progress"
```

### View Saved Stashes

```bash
git stash list
```

### Apply a Stash

```bash
git stash apply
```

### Apply and Remove the Latest Stash

```bash
git stash pop
```

### Delete All Stashes

```bash
git stash clear
```

---

## Git Cherry-pick

![Git Cherry-pick](Git%20CherryPick%20%281%29.png)

```bash
git cherry-pick <commit-id>
```

Applies a specific commit from one branch onto another branch.

---

## Git Tags

### List Tags

```bash
git tag
```

### Create a Lightweight Tag

```bash
git tag v1.0
```

### Create an Annotated Tag

```bash
git tag -a v1.0 -m "Release version 1.0"
```

### Push Tags to Remote

```bash
git push origin --tags
```

---

## Git Diff

### View Unstaged Changes

```bash
git diff
```

### View Staged Changes

```bash
git diff --staged
```

### Compare Two Commits

```bash
git diff commit1 commit2
```

---

## Undoing Changes

### Unstage a File

```bash
git restore --staged filename
```

### Discard Local Changes

```bash
git restore filename
```

### Restore All Files

```bash
git restore .
```

### Revert a Commit

```bash
git revert <commit-id>
```

---

## Cleaning Repository

### Preview Untracked Files

```bash
git clean -n
```

### Remove Untracked Files

```bash
git clean -f
```

### Remove Untracked Files and Directories

```bash
git clean -fd
```

---

## Git Aliases

### Create an Alias for `git status`

```bash
git config --global alias.st status
```

### Create an Alias for `git checkout`

```bash
git config --global alias.co checkout
```

### Create an Alias for `git branch`

```bash
git config --global alias.br branch
```

---

## Common Git Errors

![Git Error](Git%20Error%20%281%29.png)

### Failed to Push Some Refs

```bash
git pull origin main
git push origin main
```

### Merge Conflict

```bash
git add .
git commit
```

### Detached HEAD State

```bash
git switch main
```

### Remote Origin Already Exists

```bash
git remote remove origin
git remote add origin <repository-url>
```

---

## Working with GitHub

![Working on GitHub](Working-on-Github%20%281%29.png)

GitHub is a cloud-based platform for hosting Git repositories. It provides collaboration features such as pull requests, issue tracking, code reviews, and project management.

---

## Daily Git Workflow

```text
1. Create or modify files
          │
          ▼
      git status
          │
          ▼
       git add .
          │
          ▼
git commit -m "message"
          │
          ▼
   git pull origin main
          │
          ▼
git push origin main
          │
          ▼
      GitHub Repository
```

Typical daily workflow:

```bash
git status
git add .
git commit -m "Describe your changes"
git pull origin main
git push origin main
```

---

## Summary

* `git init` – Initialize a new repository.
* `git clone` – Create a local copy of a remote repository.
* `git add` – Stage changes.
* `git commit` – Save staged changes.
* `git push` – Upload changes to GitHub.
* `git pull` – Download and merge remote changes.
* `git fetch` – Download changes without merging.
* `git branch` – Create and manage branches.
* `git merge` – Combine changes from different branches.
* `git rebase` – Reapply commits on a new base.
* `git reset` – Move `HEAD` and modify repository state.
* `git stash` – Temporarily save unfinished work.
* `git cherry-pick` – Apply a specific commit.
* `git diff` – Compare changes.
* `git tag` – Create release tags.
