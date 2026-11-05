# 03 — A simple team workflow

## Example: adding a small feature

1. **Start with an updated `main`** — run `git checkout main` and `git pull origin main`.
2. **Create a task-specific branch** — run `git checkout -b feat/task-name`.
3. **Make your changes** — edit and save files in VS Code.
4. **Check and commit** — run `git status`, `git add file`, and `git commit -m "message"`.
5. **Publish your branch** — run `git push -u origin feat/task-name`.
6. **Open a Pull Request on GitHub** — choose `base: main` and `compare: feat/task-name`.
7. **Ask a teammate for a review** — they can leave comments; if changes are needed, create more commits and push to the same branch to update the PR.
8. **Merge the PR** — after review, merge it into `main` on GitHub.
9. **Update your local copy** — run `git checkout main` and `git pull origin main`.


## What if two people edit the same part of a file?

A **merge conflict** can occur when Git cannot automatically combine overlapping changes. The team needs to inspect both versions, decide on the correct final content, save the resolution, and complete the merge. **You do not need to learn detailed conflict resolution in this first workshop**; understanding why conflicts happen is sufficient.

## How can everyone work in the same repository?

The simplest approach for this workshop is a **shared repository**. The instructor invites participants as collaborators with write access. Everyone can then push their own branch and open a PR.
