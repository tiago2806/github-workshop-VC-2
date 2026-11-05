# 05 — Common Git problems

## `git` is not recognized in the terminal

Git may not be installed or may not be available on your system `PATH`. Install it from https://git-scm.com/downloads, restart VS Code, and check `git --version`.

## `Author identity unknown` when committing

Configure your name and email:

```bash
git config --global user.name "Your Name"
git config --global user.email "your-email@example.com"
```

## Authentication or permission error when pushing

- Make sure you have authenticated with GitHub when prompted.
- Check that you accepted the invitation to collaborate on the repository.
- **Your normal GitHub account password cannot be used for Git authentication over HTTPS.** Depending on your setup, you may authenticate through a browser or a credential manager.

## `fatal: not a git repository`

You are probably outside the repository directory. After cloning, run:

```bash
cd github-workshop-VC-2-english
git status
```

## `nothing to commit, working tree clean`

There are no new changes to commit in your working tree or staging area. Check that you created or saved the correct file, then run `git status`.

## `rejected` / `non-fast-forward` when pushing

The remote branch may contain commits that you do not have locally. Do not use `--force` as an automatic fix. Ask for help synchronizing the branches and resolving differences without losing work.

## `merge conflict`

Git found changes that cannot be combined automatically. In this workshop, the goal is to recognize the problem and ask for help: inspect both versions and resolve the differences rather than deleting changes blindly.

## `git pull` updated the wrong branch

`git pull origin main` integrates remote `main` into **whichever local branch is currently checked out**, even if that branch is not `main`. Check your current branch with `git status`, then run `git switch main` before pulling if your goal is to update your local `main`.
