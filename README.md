# Git & GitHub Workshop 🚀

**Learn how to collaborate on a team project using Git, GitHub, and the VS Code terminal.**

> **Audience:** Beginners. No programming experience is required.
>
> **Suggested duration:** 60 minutes. By the end, you should be able to make a real contribution to this repository.

## What will you learn?

1. Explain the difference between **Git** and **GitHub**.
2. Understand **repositories**, **commits**, **branches**, **merges**, and **Pull Requests (PRs)**.
3. Run essential Git commands in the **VS Code integrated terminal**.
4. Create a branch, save and publish changes, open a PR, and collaborate with teammates.
5. Follow simple best practices for team projects.

## Workshop agenda

| Time | Topic | Material |
| --- | --- | --- |
| 0–5 min | Git, GitHub, and repositories | [Core concepts](docs/01-concepts.md) |
| 5–15 min | Local vs. remote, commits, and branches | [Core concepts](docs/01-concepts.md) |
| 15–30 min | Essential Git commands in VS Code | [Commands](docs/02-commands.md) |
| 30–40 min | Team workflow with branches and PRs | [Team workflow](docs/03-team-workflow.md) |
| 40–55 min | Hands-on contribution to this repository | [Exercise](exercises/README.md) |
| 55–60 min | Best practices and questions | [Best practices](docs/04-best-practices.md) |

## Git vs. GitHub: the short version

- **Git** is a version control system. It tracks changes, records commits, and manages branches on your computer, even without an internet connection.
- **GitHub** is an online platform that hosts Git repositories and provides collaboration features such as **Pull Requests** and **code reviews**.

## The essential workflow

```text
GitHub (main)
     │
     ▼
Clone the repository and update your local main
     │
     ▼
Create a branch for your task
     │
     ▼
Edit files → git add → git commit
     │
     ▼
git push → open a Pull Request on GitHub
     │
     ▼
Code review → merge into main
     │
     ▼
Switch to your local main → git pull
```

## Getting started

**Before the workshop:** Create a [GitHub account](https://github.com), install [Git](https://git-scm.com/downloads) and [VS Code](https://code.visualstudio.com), and make sure the instructor has granted you write access to this repository.

Open the project folder in VS Code and select **Terminal → New Terminal**. Check your Git installation:

```bash
git --version
```

Then follow the [hands-on exercise](exercises/README.md). If you have not configured Git yet, see [Initial setup](docs/02-commands.md#0-initial-setup-one-time).

## Learning materials

- 📘 [01 — Core concepts](docs/01-concepts.md)
- 💻 [02 — Essential commands (cheat sheet)](docs/02-commands.md)
- 🤝 [03 — Working in a team](docs/03-team-workflow.md)
- ✅ [04 — Best practices](docs/04-best-practices.md)
- 🛠️ [05 — Common problems](docs/05-common-problems.md)
- 🧪 [Hands-on exercise](exercises/README.md)
- 🎤 [Instructor guide](INSTRUCTOR-GUIDE.md)

## Remember

**`git pull` is not a Pull Request.** `git pull` fetches remote changes and integrates them into your current local branch. A **Pull Request** is a proposal on GitHub to review and merge changes from one branch into another.

### Official references

- [About Git — GitHub Docs](https://docs.github.com/en/get-started/using-git/about-git)
- [About Pull Requests — GitHub Docs](https://docs.github.com/en/pull-requests/get-started/about-pull-requests)
- [VS Code integrated terminal](https://code.visualstudio.com/docs/terminal/basics)
- [Git command reference](https://git-scm.com/docs)
