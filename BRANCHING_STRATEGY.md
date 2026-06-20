# Git Branching & Workflow Strategy

This repository follows a **Feature-Branch / Simplified Gitflow** model to ensure stable releases and clean code reviews.

## 1. Core Branches
* `main` — **[Protected]** The source of truth. Code here is always production-ready and deployable. Direct pushes are disabled.
* `dev` — **[Protected]** The active integration branch. All completed feature branches are merged here first for testing.

## 2. Supporting Branches 

When picking up a ticket/task, create a new branch off of `dev` using the following naming conventions:

| Branch Type | Naming Convention | Example | Use Case |
| :--- | :--- | :--- | :--- |
| **Feature** | `feature/[issue#]-[short-desc]` | `feature/12-google-auth` | Building a new feature |
| **Bugfix** | `bugfix/[issue#]-[short-desc]` | `bugfix/34-header-typo` | Fixing a non-critical bug |
| **Hotfix** | `hotfix/[short-desc]` | `hotfix/login-crash` | **Urgent** prod fix (branches off `main`) |
| **Chore** | `chore/[short-desc]` | `chore/update-readme` | Maintenance / Docs / Configs |

## 3. The Golden Rules
1. **Never push directly to `main` or `dev`.** 2. Always make sure your local `dev` branch is `git pull`ed up-to-date before branching off of it.
3. Keep Pull Requests small. If a PR touches more than 15 files, break it into two smaller tasks.
4. Delete your feature branch on GitHub immediately after the PR is successfully merged.
