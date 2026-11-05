# 01 — Core concepts

## Git and GitHub are not the same thing

**Git** is a version control system. It records how a project changes over time and lets you work on different versions without losing the history. **GitHub** is an online platform that hosts Git repositories and supports collaboration through features such as Pull Requests and code reviews.

You can use Git without GitHub. Commits can be saved locally without an internet connection; to share them, you typically use a remote repository.

## Essential vocabulary

| Term | Simple explanation |
| --- | --- |
| **Repository (repo)** | A project tracked by Git, including its version history. |
| **Local** | The copy of the project on your computer. |
| **Remote** | A repository accessible over a network, usually on GitHub. |
| **`origin`** | The conventional name for the main remote, commonly set by `git clone`. |
| **Commit** | A snapshot of staged changes, recorded with a descriptive message. |
| **Branch** | A separate line of development that lets you work on a task without immediately changing `main`. |
| **`main`** | The usual name of a project's primary branch. |
| **Merge** | Combining changes from one branch into another. |
| **Pull Request (PR)** | A proposal to merge changes from one branch into another, allowing discussion and review first. |

## What happens when you edit a file?

```text
Modified file (working directory)
                │
             git add
                ▼
Selected changes (staging area)
                │
             git commit
                ▼
Commit saved in your LOCAL history
                │
             git push
                ▼
Commit published on GitHub (REMOTE)
```

- `git add` **does not** send anything to GitHub.
- `git commit` **does not** send anything to GitHub.
- `git push` sends local commits to the remote repository.

## Why do teams use branches?

Imagine three teammates working on the same project:

- One builds a feature on `feat/login`.
- Another fixes a bug on `fix/menu`.
- A third improves documentation on `docs/readme`.

They can work in parallel, commit their changes, and push their branches. In the workshop workflow, `main` receives those changes only after the PRs have been reviewed and merged.

## `git pull` vs. Pull Request

| | `git pull` | Pull Request (PR) |
| --- | --- | --- |
| **What is it?** | A Git command | A GitHub collaboration feature |
| **Purpose** | Fetch remote changes and integrate them into the current local branch | Propose, discuss, and review changes before merging them into another branch |
| **Where does it happen?** | In the terminal | On GitHub (in your browser for this workshop) |

**Example:** A teammate merges a PR into `main` on GitHub. You run `git checkout main` on your vs code terminal followed by `git pull origin main` to get those changes on your computer.
