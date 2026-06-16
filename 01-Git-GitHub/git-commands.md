

## Branch Management 

### List All Local and Remote Branches

```bash
git branch -a
```

Displays all local and remote branches.

### List Only Remote Branches

```bash
git branch -r
```

Shows all branches available on the remote repository.

### Switch to a Branch (Modern Way)

```bash
git switch branch-name
```

Switches to the specified branch.

### Create and Switch to a New Branch

```bash
git switch -c branch-name
```

Creates and switches to a new branch.

---

## Rebasing

### Rebase Current Branch onto Main

```bash
git rebase main
```

Moves the current branch commits on top of the latest `main` branch.

### Interactive Rebase

```bash
git rebase -i HEAD~3
```

Interactively edit, reorder, squash, or remove the last 3 commits.

### Continue Rebase

```bash
git rebase --continue
```

Continues the rebase process after resolving conflicts.

### Abort Rebase

```bash
git rebase --abort
```

Cancels the current rebase operation.

---

## Git Tags

### List All Tags

```bash
git tag
```

Displays all available tags.

### Create a Lightweight Tag

```bash
git tag v1.0
```

Creates a simple tag named `v1.0`.

### Create an Annotated Tag

```bash
git tag -a v1.0 -m "Release version 1.0"
```

Creates a tag with additional metadata.

### Push Tags to GitHub

```bash
git push origin --tags
```

Uploads all local tags to the remote repository.

---

## Stashing (Advanced)

### Save Stash with a Message

```bash
git stash push -m "Work in progress"
```

Temporarily saves changes with a descriptive message.

### Show All Stashes

```bash
git stash list
```

Displays all saved stashes.

### View Stash Details

```bash
git stash show
```

Shows information about the latest stash.

### Remove All Stashes

```bash
git stash clear
```

Deletes all stashed changes.

---

## Remote Repository Management

### Show Remote Repository URLs

```bash
git remote -v
```

Displays the URLs of all configured remote repositories.

### Remove a Remote Repository

```bash
git remote remove origin
```

Removes the remote named `origin`.

### Change Remote Repository URL

```bash
git remote set-url origin <new-repository-url>
```

Updates the URL of the remote repository.

### Show Detailed Remote Information

```bash
git remote show origin
```

Displays detailed information about the `origin` remote.

---

## Cherry-pick

### Apply a Specific Commit

```bash
git cherry-pick <commit-id>
```

Applies a specific commit from another branch to the current branch.

---

## Useful Git Log Commands

### Show Commit History as a Graph

```bash
git log --graph --oneline --decorate --all
```

Displays the commit history in a graphical tree format.

### Show Last 5 Commits

```bash
git log -5
```

Displays the last five commits.

### Show Details of a Commit

```bash
git show <commit-id>
```

Shows detailed information about a specific commit.

---

## Cleaning Untracked Files

### Preview Files to be Removed

```bash
git clean -n
```

Shows which untracked files would be deleted.

### Remove Untracked Files

```bash
git clean -f
```

Deletes all untracked files.

### Remove Untracked Files and Directories

```bash
git clean -fd
```

Deletes all untracked files and directories.

---

## Git Aliases

### Create a Shortcut for git status

```bash
git config --global alias.st status
```

### Create a Shortcut for git checkout

```bash
git config --global alias.co checkout
```

### Create a Shortcut for git branch

```bash
git config --global alias.br branch
```

Aliases help reduce typing by creating shorter versions of commonly used Git commands.

---

## Daily Git Workflow Example

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

---

## Pro Tip 💡

Before pushing your changes, always run:

```bash
git status
git pull origin main
git push origin main
```

This helps you avoid merge conflicts and ensures your local repository is up to date with the remote repository.
