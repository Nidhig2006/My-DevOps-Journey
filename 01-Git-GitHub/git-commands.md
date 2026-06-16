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

![Git Workflow](images/git-basic-commands(1).png)

The above diagram illustrates the standard Git workflow from modifying files to pushing changes to GitHub.

---

## Git Stages

![Git Stages](images/git-stages.png)

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

Sets the global username used in commits.

### Configure Email

```bash
git config --global user.email "your-email@example.com"
```

Sets the global email address associated with commits.

### View Git Configuration

```bash
git config --list
```

Displays all configured Git settings.

### Set Default Branch Name

```bash
git config --global init.defaultBranch main
```

Sets `main` as the default branch name for newly created repositories.

---

## Repository Initialization

### Initialize a New Repository

```bash
git init
```

Creates a new Git repository in the current directory.

### Clone an Existing Repository

```bash
git clone <repository-url>
```

Creates a local copy of a remote repository.

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

Displays:

* Current branch.
* Modified files.
* Untracked files.
* Staged files.

### View Commit History

```bash
git log
```

Displays the complete commit history.

### View Commit History in One Line

```bash
git log --oneline
```

Displays a compact commit history.

### View Commit History as a Graph

```bash
git log --graph --oneline --decorate --all
```

Displays the branch structure and commit history graphically.

### View HEAD History

```bash
git reflog
```

Shows all recent updates to the `HEAD` pointer.

---

## Staging Changes

### Add a Specific File

```bash
git add filename
```

Stages a single file.

### Add All Files

```bash
git add .
```

Stages all new and modified files.

### Add All Changes

```bash
git add -A
```

Stages new, modified, and deleted files.

### Unstage a File

```bash
git restore --staged filename
```

Removes a file from the staging area while keeping local changes.

---

## Committing Changes

### Create a Commit

```bash
git commit -m "Commit message"
```

Creates a new commit from staged changes.

### Commit Tracked Files Directly

```bash
git commit -am "Updated project"
```

Stages and commits all tracked files.

### Modify the Last Commit

```bash
git commit --amend
```

Updates the previous commit.

---

## Remote Repository Operations

### Add a Remote Repository

```bash
git remote add origin <repository-url>
```

Adds a remote repository named `origin`.

### View Remote Repositories

```bash
git remote -v
```

Displays configured remote URLs.

### Change the Remote URL

```bash
git remote set-url origin <new-url>
```

Updates the URL of the remote repository.

### Remove a Remote Repository

```bash
git remote remove origin
```

Removes the configured remote.

### Push Changes

```bash
git push origin main
```

Uploads local commits to the remote repository.

### Push and Set Upstream Branch

```bash
git push -u origin main
```

Pushes changes and creates a tracking relationship.

### Pull Latest Changes

```bash
git pull origin main
```

Downloads and merges remote changes.

### Fetch Latest Changes

```bash
git fetch origin
```

Downloads changes without merging them.

---

## Branch Management

![Git Branches](images/git-branches.png)

Branches allow developers to work independently without affecting the main codebase.

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

![Git Merge vs Git Rebase](images/git-merge-vs-rebase.png)

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

![Git Reset](images/git-reset.png)

`git reset` changes the current `HEAD` pointer to a specified commit.

### Soft Reset

![Git Soft Reset](images/git-soft-reset.png)

```bash
git reset --soft HEAD~1
```

Moves `HEAD` while keeping all changes staged.

### Mixed Reset

![Git Mixed Reset](images/git-mixed-reset.png)

```bash
git reset --mixed HEAD~1
```

Moves `HEAD` and unstages changes while preserving files.

### Hard Reset

![Git Hard Reset](images/git-hard-reset.png)

```bash
git reset --hard HEAD~1
```

Moves `HEAD` and permanently removes staged and local changes.

---

## Git Stash

![Git Stash](images/git-stash.png)

Temporarily stores uncommitted changes.

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

![Git Cherry-pick](images/git-cherry-pick.png)

Applies a specific commit from one branch onto another branch.

```bash
git cherry-pick <commit-id>
```

This command is useful when only a single commit needs to be transferred.

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

Creates a new commit that reverses the specified commit.

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

Aliases reduce typing by creating short forms for commonly used commands.

---

## Common Git Errors

![Git Error](images/git-error.png)

### Failed to Push Some Refs

```bash
git pull origin main
git push origin main
```

### Merge Conflict

Resolve the conflicting files manually, then run:

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

