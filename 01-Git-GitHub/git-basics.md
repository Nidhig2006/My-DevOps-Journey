# 📘 Git & GitHub Basics

## What is Git?

Git is a **distributed version control system (DVCS)** that helps developers track changes in source code, collaborate with others, and manage different versions of a project efficiently.

Git was created by **Linus Torvalds** in 2005 for the development of the Linux kernel.

### Why do we use Git?
- Track changes in files and source code.
- Collaborate with multiple developers.
- Maintain version history.
- Revert to previous versions if something goes wrong.
- Work on new features without affecting the main codebase.

---

## What is GitHub?

GitHub is a **cloud-based platform** that hosts Git repositories. It provides features like collaboration, pull requests, issue tracking, project management, and CI/CD integration.

In simple words:
- **Git** = Version Control System.
- **GitHub** = A platform to store and manage Git repositories online.

---

## Version Control System (VCS)

A Version Control System helps developers manage changes to files over time. It records every modification, allowing you to compare versions, restore old versions, and collaborate with others.

### Types of Version Control Systems

### 1. Local Version Control System
- Stores versions on a local machine.
- Not suitable for team collaboration.

### 2. Centralized Version Control System (CVCS)
- Uses a central server to store all versions.
- Developers connect to the server to get or commit changes.
- Examples: SVN (Subversion), CVS.

### 3. Distributed Version Control System (DVCS)
- Every developer has a complete copy of the repository, including its history.
- Works even when offline.
- Git is the most popular DVCS.

---

## Centralized vs Distributed Version Control

| Feature | Centralized VCS | Distributed VCS (Git) |
|----------|-----------------|-----------------------|
| Repository | Single central repository | Every user has a full copy |
| Offline Work | Limited | Fully supported |
| Speed | Slower | Faster |
| Backup | Single point of failure | Multiple copies available |
| Collaboration | Depends on central server | Flexible and efficient |

---

## Git Architecture

Git mainly works with three areas:

### 1. Working Directory
The working directory is where you create, edit, and delete files. It contains the current version of your project that you are actively working on.

### 2. Staging Area (Index)
The staging area acts as a preparation zone where you add the changes that you want to include in the next commit.

### 3. Local Repository
The local repository stores all committed changes and the complete history of your project on your local machine.

### 4. Remote Repository
A remote repository (such as GitHub) is a copy of your local repository hosted on a server, allowing collaboration and backup.

---

## Git Workflow

The basic Git workflow is:

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
 Remote Repository (GitHub)
```

Similarly, when you want to download the latest changes from GitHub:

```text
GitHub Repository
       │
       ▼
   git pull
       │
       ▼
 Local Repository
       │
       ▼
 Working Directory
```

---

## Basic Git Terminology

| Term | Description |
|------|-------------|
| Repository (Repo) | A storage location for your project and its history. |
| Commit | A snapshot of changes at a specific point in time. |
| Branch | An independent line of development. |
| Merge | Combining changes from one branch into another. |
| Clone | Creating a local copy of a remote repository. |
| Push | Uploading local commits to a remote repository. |
| Pull | Downloading and merging changes from a remote repository. |
| Fetch | Downloading changes without merging them. |
| Staging Area | Temporary area where changes are prepared before committing. |

---

## Advantages of Git

- Free and open source.
- Fast and lightweight.
- Supports distributed development.
- Easy branching and merging.
- Maintains complete project history.
- Excellent support for collaboration.
- Integrates with platforms like GitHub, GitLab, and Bitbucket.

---

## Git vs GitHub

| Git | GitHub |
|-----|---------|
| Version control system | Cloud-based Git hosting platform |
| Installed locally | Accessed through the web |
| Tracks file changes | Stores and shares repositories |
| Works offline | Requires internet for remote operations |
| Created by Linus Torvalds | Owned by Microsoft |

---

## Summary

- Git is a distributed version control system used to track changes in projects.
- GitHub is a cloud platform used to host and collaborate on Git repositories.
- Git uses the concepts of Working Directory, Staging Area, Local Repository, and Remote Repository.
- The basic Git workflow follows: **Edit → Add → Commit → Push**.
- Git makes collaboration, version tracking, and project management easier and more efficient.
