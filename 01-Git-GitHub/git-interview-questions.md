## Git Basics

<details>
<summary><strong>What is the difference between Git and GitHub?</strong></summary>

**Git** is a distributed version control system used to track changes in source code.

**GitHub** is a cloud-based platform that hosts Git repositories and provides collaboration features like pull requests, issues, and actions.

| Git | GitHub |
|-----|---------|
| Version Control System | Git Repository Hosting Platform |
| Works locally | Cloud-based service |
| Tracks file changes | Stores and manages repositories |

</details>

---

<details>
<summary><strong>Why do we use Git?</strong></summary>

Git is used to:
- Track changes in source code.
- Collaborate with multiple developers.
- Maintain version history.
- Create and manage branches.
- Revert to previous versions if necessary.
- Prevent accidental data loss.

</details>

---

<details>
<summary><strong>What is a commit in Git?</strong></summary>

A commit is a snapshot of the changes made to a repository at a specific point in time. Each commit has a unique SHA-1 hash that identifies it.

Example:
```bash
git commit -m "Added Git interview questions"
```

</details>

---

<details>
<summary><strong>What is a branch in Git?</strong></summary>

A branch is an independent line of development. It allows developers to work on new features or bug fixes without affecting the main branch.

The default branch is usually called `main`.

</details>

---

<details>
<summary><strong>What is HEAD in Git?</strong></summary>

`HEAD` is a pointer that refers to the latest commit on the currently checked-out branch.

You can view the current branch using:

```bash
git branch
```

The branch marked with `*` is where `HEAD` is pointing.

</details>

---

<details>
<summary><strong>What is the difference between tracked and untracked files?</strong></summary>

- **Tracked files** are files that Git already knows about and monitors for changes.
- **Untracked files** are new files that have not been added to the staging area.

You can check them using:

```bash
git status
```

</details>

---

<details>
<summary><strong>What is the difference between a local repository and a remote repository?</strong></summary>

- **Local Repository:** Exists on your computer and stores all commits and project history.
- **Remote Repository:** Hosted on platforms like GitHub, GitLab, or Bitbucket for collaboration and backup.

</details>

---

<details>
<summary><strong>What happens when you run <code>git add .</code>?</strong></summary>

The command stages all new, modified, and deleted files in the current directory for the next commit.

```bash
git add .
```

After staging, verify using:

```bash
git status
```

</details>

---

<details>
<summary><strong>What happens when you run <code>git commit</code>?</strong></summary>

`git commit` creates a snapshot of all staged changes and stores them permanently in the local repository.

Example:

```bash
git commit -m "Initial commit"
```

</details>

---

<details>
<summary><strong>What is the difference between <code>git clone</code> and <code>git fork</code>?</strong></summary>

- **git clone** creates a local copy of an existing repository.
- **Fork** creates a personal copy of someone else's repository on GitHub.

Forking is commonly used when contributing to open-source projects.

</details>

---

<details>
<summary><strong>What is the purpose of <code>git log</code>?</strong></summary>

`git log` displays the commit history of the repository.

Useful variations:

```bash
git log
git log --oneline
git log --graph --decorate --all
```

</details>

---

<details>
<summary><strong>What is the difference between <code>git status</code> and <code>git diff</code>?</strong></summary>

| git status | git diff |
|-------------|-----------|
| Shows the state of the repository. | Shows the exact line-by-line changes. |
| Lists staged and unstaged files. | Displays code differences. |

</details>

---

<details>
<summary><strong>What is the purpose of the <code>git reflog</code> command?</strong></summary>

`git reflog` records all movements of `HEAD` and helps recover lost commits or branches after operations like reset or rebase.

```bash
git reflog
```

</details>

---

<details>
<summary><strong>How do you rename a branch in Git?</strong></summary>

Rename the current branch:

```bash
git branch -m new-branch-name
```

Rename another branch:

```bash
git branch -m old-branch-name new-branch-name
```

</details>

---

<details>
<summary><strong>What is the difference between <code>git pull</code> and <code>git clone</code>?</strong></summary>

- `git clone` creates a new local copy of a remote repository.
- `git pull` updates an existing local repository by downloading and merging changes from the remote repository.

</details>

---

<details>
<summary><strong>How can you see which branch you are currently working on?</strong></summary>

Run:

```bash
git branch
```

The branch marked with `*` is the currently active branch.

Alternatively:

```bash
git status
```

It also displays the current branch name.

</details>

---

<details>
<summary><strong>What is a merge conflict?</strong></summary>

A merge conflict occurs when Git cannot automatically combine changes from two branches because the same part of a file was modified differently.

The conflict must be resolved manually before completing the merge.

</details>

---

<details>
<summary><strong>What are some advantages of using Git?</strong></summary>

- Distributed architecture.
- Fast and lightweight.
- Easy branching and merging.
- Complete version history.
- Supports collaboration.
- Easy backup and recovery.
- Free and open source.

</details>

---

<details>
<summary><strong>What is the typical Git workflow?</strong></summary>

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

Common commands:

```bash
git status
git add .
git commit -m "message"
git push origin main
```

</details>
