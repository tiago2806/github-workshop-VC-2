# 03 — A simple team workflow

## Example: adding a small feature

1. **Start with an updated `main`** — run `git switch main` and `git pull origin main`.
2. **Create a task-specific branch** — run `git switch -c feat/task-name`.
3. **Make your changes** — edit and save files in VS Code.
4. **Check and commit** — run `git status`, `git add file`, and `git commit -m "message"`.
5. **Publish your branch** — run `git push -u origin feat/task-name`.
6. **Open a Pull Request on GitHub** — choose `base: main` and `compare: feat/task-name`.
7. **Ask a teammate for a review** — they can leave comments; if changes are needed, create more commits and push to the same branch to update the PR.
8. **Merge the PR** — after review, merge it into `main` on GitHub.
9. **Update your local copy** — run `git switch main` and `git pull origin main`.

## Why does this work?

Branches separate tasks. Commits preserve changes and their history. Pull Requests let teammates review what will be added to `main` before merging.

**Example branch names**

- `feat/login` — new feature
- `fix/navbar` — bug fix
- `docs/readme` — documentation

## What is a code review?

Before merging, a teammate can check whether:

- The PR addresses the intended task.
- The changes are understandable.
- There are no unnecessary changes or confidential files.
- Existing functionality still works.

For this session, **one simple peer review per PR** is enough.

## What if two people edit the same part of a file?

A **merge conflict** can occur when Git cannot automatically combine overlapping changes. The team needs to inspect both versions, decide on the correct final content, save the resolution, and complete the merge. **You do not need to learn detailed conflict resolution in this first workshop**; understanding why conflicts happen is sufficient.

## How can everyone work in the same repository?

The simplest approach for this workshop is a **shared repository**. The instructor invites participants as collaborators with write access. Everyone can then push their own branch and open a PR.

Someone **without write permission** would typically create a **fork** and propose changes with a PR from their fork. That workflow is beyond the scope of this beginner session.

> `git pull` updates your local repository. **It does not ask teammates to accept your code.** That is what a Pull Request is for.
