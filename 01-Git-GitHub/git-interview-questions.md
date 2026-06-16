
## Git Basics

<details>
<summary>What is Git?</summary>

Git is a distributed version control system that tracks changes in source code and allows multiple developers to collaborate efficiently.
</details>

<details>
<summary>What is the difference between Git and GitHub?</summary>

Git is a version control tool, while GitHub is a cloud platform that hosts Git repositories and provides collaboration features.
</details>

<details>
<summary>Why is Git called a distributed version control system?</summary>

Because every developer has a complete copy of the repository, including the full commit history.
</details>

<details>
<summary>How do you initialize a Git repository?</summary>

Use:
```bash
git init
```
</details>

<details>
<summary>How do you clone a remote repository?</summary>

Use:
```bash
git clone <repository-url>
```
</details>

<details>
<summary>What does the .git directory contain?</summary>

It contains the Git object database, commit history, references, configuration files, and metadata required to manage the repository.
</details>

<details>
<summary>What is a commit?</summary>

A commit is a snapshot of the project's tracked files at a specific point in time.
</details>

<details>
<summary>What is the purpose of git status?</summary>

It shows the current branch, staged changes, unstaged changes, and untracked files.
</details>

<details>
<summary>What is the difference between tracked and untracked files?</summary>

Tracked files are already managed by Git, while untracked files are new files that Git has not started tracking.
</details>

<details>
<summary>What is the purpose of git add?</summary>

It moves changes from the working directory to the staging area.
</details>

---

## Staging and Commit

<details>
<summary>What is the staging area?</summary>

The staging area (index) is an intermediate area where changes are prepared before creating a commit.
</details>

<details>
<summary>What is the difference between git add . and git add -A?</summary>

`git add .` stages changes in the current directory, while `git add -A` stages all changes including deletions across the repository.
</details>

<details>
<summary>What does git commit -m do?</summary>

It creates a new commit with the specified commit message.
</details>

<details>
<summary>What does git commit --amend do?</summary>

It modifies the most recent commit by changing its message or adding newly staged changes.
</details>

<details>
<summary>Can you commit without staging?</summary>

Yes, by using:
```bash
git commit -am "message"
```
This works only for tracked files.
</details>

---

## Branching

<details>
<summary>What is a branch in Git?</summary>

A branch is a lightweight movable pointer to a commit.
</details>

<details>
<summary>Why do we use branches?</summary>

Branches allow developers to work on new features or bug fixes independently without affecting the main codebase.
</details>

<details>
<summary>How do you create a new branch?</summary>

```bash
git branch branch-name
```
</details>

<details>
<summary>How do you switch branches?</summary>

```bash
git switch branch-name
```

or

```bash
git checkout branch-name
```
</details>

<details>
<summary>How do you create and switch to a new branch?</summary>

```bash
git switch -c branch-name
```
</details>

<details>
<summary>What is the difference between git switch and git checkout?</summary>

`git switch` is specifically for branch switching, while `git checkout` can switch branches and restore files.
</details>

---

## Merge and Rebase

<details>
<summary>What is a merge in Git?</summary>

A merge combines changes from one branch into another and usually creates a merge commit.
</details>

<details>
<summary>What is rebase?</summary>

Rebase moves or reapplies commits onto another base commit, creating a linear history.
</details>

<details>
<summary>What is the difference between merge and rebase?</summary>

Merge preserves branch history and creates a merge commit. Rebase rewrites history and creates a cleaner linear commit history.
</details>

<details>
<summary>What is a merge conflict?</summary>

A merge conflict occurs when Git cannot automatically combine changes because the same lines were modified in different branches.
</details>

<details>
<summary>How do you resolve merge conflicts?</summary>

Edit the conflicting files manually, remove conflict markers, then run:

```bash
git add .
git commit
```
</details>

<details>
<summary>What does git rebase --continue do?</summary>

It continues the rebase process after conflicts have been resolved.
</details>

<details>
<summary>What does git rebase --abort do?</summary>

It cancels the current rebase operation and returns the repository to its previous state.
</details>

---

## Reset, Revert and Restore

<details>
<summary>What is the difference between git reset and git revert?</summary>

`git reset` changes commit history, while `git revert` creates a new commit that undoes the changes of a previous commit.
</details>

<details>
<summary>What is the difference between soft, mixed, and hard reset?</summary>

- Soft: Removes commit, keeps changes staged.
- Mixed: Removes commit, keeps changes unstaged.
- Hard: Removes commit and deletes local changes.
</details>

<details>
<summary>What does git restore do?</summary>

It restores files in the working directory or unstages files from the staging area.
</details>

<details>
<summary>When would you use git revert instead of git reset?</summary>

When the commit has already been pushed to a shared remote repository and history should not be rewritten.
</details>

---

## Stash

<details>
<summary>What is git stash?</summary>

Git stash temporarily saves uncommitted changes without creating a commit.
</details>

<details>
<summary>How do you list all stashes?</summary>

```bash
git stash list
```
</details>

<details>
<summary>What is the difference between git stash apply and git stash pop?</summary>

`apply` restores the stash without deleting it. `pop` restores and removes it from the stash list.
</details>

---

## GitHub and Remote Repositories

<details>
<summary>What is origin in Git?</summary>

`origin` is the default alias for the remote repository from which a project was cloned.
</details>

<details>
<summary>What is upstream in Git?</summary>

An upstream branch is the remote branch that your local branch tracks.
</details>

<details>
<summary>What is the difference between git fetch and git pull?</summary>

`git fetch` downloads remote changes without merging them. `git pull` downloads and merges changes automatically.
</details>

<details>
<summary>How do you view configured remotes?</summary>

```bash
git remote -v
```
</details>

<details>
<summary>How do you remove a remote repository?</summary>

```bash
git remote remove origin
```
</details>

<details>
<summary>What is a pull request?</summary>

A pull request is a request to review and merge changes from one branch into another, commonly used in GitHub workflows.
</details>

---

## Git Internals

<details>
<summary>What is HEAD in Git?</summary>

HEAD is a pointer that refers to the currently checked-out commit or branch.
</details>

<details>
<summary>What is the Git object database?</summary>

It is the internal storage where Git saves blobs, trees, commits, and tags.
</details>

<details>
<summary>What are Git blobs, trees, and commits?</summary>

- Blob: Stores file content.
- Tree: Stores directory structure.
- Commit: Stores metadata and references to tree objects.
</details>

<details>
<summary>What is git reflog?</summary>

It records all changes made to the HEAD reference and can help recover lost commits.
</details>

<details>
<summary>Can you recover a deleted commit?</summary>

Yes, in many cases it can be recovered using `git reflog`.
</details>

---

## Scenario-Based Questions

<details>
<summary>You accidentally committed to the wrong branch. What would you do?</summary>

Create a new branch from the current state, switch back to the correct branch, and use `git reset` or `git cherry-pick` as appropriate.
</details>

<details>
<summary>You committed a file containing sensitive information. How would you handle it?</summary>

Remove the file, rewrite history using tools like `git filter-repo` or `BFG Repo-Cleaner`, and rotate any exposed credentials.
</details>

<details>
<summary>You want to save your work without committing. What command would you use?</summary>

Use:
```bash
git stash
```
</details>

<details>
<summary>You want to apply one commit from another branch without merging the entire branch. What should you use?</summary>

Use:
```bash
git cherry-pick <commit-id>
```
</details>

<details>
<summary>You accidentally deleted a branch. Can you recover it?</summary>

Yes. Use `git reflog` to locate the last commit and recreate the branch from that commit.
</details>

---

## Advanced Questions

<details>
<summary>What is a detached HEAD state?</summary>

A detached HEAD occurs when HEAD points directly to a commit instead of a branch.
</details>

<details>
<summary>What is git bisect used for?</summary>

It performs a binary search through commit history to identify the commit that introduced a bug.
</details>

<details>
<summary>What are Git tags used for?</summary>

Tags are used to mark important points in history, typically software releases.
</details>

<details>
<summary>What is the difference between annotated and lightweight tags?</summary>

Annotated tags contain metadata (author, date, message), while lightweight tags are simple references to commits.
</details>

<details>
<summary>What are some Git best practices?</summary>

- Commit frequently with meaningful messages.
- Use feature branches.
- Pull before pushing.
- Avoid force pushing to shared branches.
- Keep commits small and focused.
- Use `.gitignore` correctly.
</details>
