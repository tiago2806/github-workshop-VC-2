# 02 — Essential Git commands in the VS Code terminal

In VS Code, open your project folder and select **Terminal → New Terminal**. Run the following commands in the integrated terminal (PowerShell, Bash, etc.).


## 1. Quick reference

| Command | What does it do? |
| --- | --- |
| `git clone URL` | Downloads a remote repository to your computer. |
| `git status` | Shows your current branch and modified, staged, or untracked files. |
| `git branch` | Lists local branches. |
| `git checkout main` | Switches to the local `main` branch. |
| `git pull origin main` | Fetches remote changes from `main` and integrates them into your **current local branch** (run this while on `main` for this workshop). |
| `git checkout -b branch-name` | Creates a new branch and switches to it. |
| `git add file` | Stages changes to a file for the next commit. |
| `git commit -m "message"` | Saves the staged changes as a **local** commit. |
| `git push -u origin branch-name` | Publishes a branch and sets up its upstream tracking branch. Used when it is the first time pushing changes into a new branch. The following times, you just need `git push` |
| `git push` | Sends new commits to the configured upstream remote branch. |

### Useful, but optional for this workshop

| Command | What does it do? |
| `git branch -d branch-name` | Deletes a **local** branch that has already been merged. |
TBD

## 2. Full example: making a contribution

**Replace `YOUR-USERNAME` with your GitHub username.** Use it in the branch and file names (no spaces).

```bash
# Download the project and enter its folder
git clone https://github.com/tiago2806/github-workshop-VC-2-english.git
cd github-workshop-VC-2-english

# Start from an up-to-date main branch
git checkout main
git pull origin main

# Create a branch for your task
git checkout -b feature/profile-YOUR-USERNAME

# Now create/edit participants/YOUR-USERNAME.md in VS Code

# Check what has changed
git status

# Stage only your file
git add participants/YOUR-USERNAME.md

# Save the change in local history
git commit -m "Add participant profile"

# Publish your branch on GitHub
git push -u origin feat/profile-YOUR-USERNAME
```

**Note:** Lines beginning with `#` are comments in Bash and PowerShell; you do not need to run them. Create and save the file in the editor before using `git add`.

After pushing, open the repository in your **browser** to create the Pull Request: select your branch and click **Compare & pull request** (or **New pull request**), with **base: `main`**.

In a PR:
**base** -> The branch into which you want to merge your changes (usually main).
**head** -> The branch containing the changes you want to merge into the base branch (usually a feature branch).

## 3. After your PR is merged

```bash
git checkout main
git pull origin main
```

This updates your local `main` with the work that has been merged on GitHub.
