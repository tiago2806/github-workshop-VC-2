# 04 — Simple best practices for team projects

## Recommended rules

1. **Do not work directly on `main`** for ordinary tasks; use a separate branch for each task.
2. **Update `main` before starting** (`git switch main` followed by `git pull origin main`).
3. **Use clear branch names**, such as `feat/login` or `fix/login-error`.
4. **Make small commits with descriptive messages**, such as `Fix login validation` instead of `changes`.
5. **Check your files before committing** with `git status` and, ideally, `git diff`.
6. **Keep Pull Requests focused:** one main purpose or task per PR.
7. **Ask for peer review before merging** into `main`.
8. **Never commit passwords, tokens, API keys, or `.env` files.** Use `.gitignore`, but remember that ignoring a file does not remove secrets that were already committed.
9. **Communicate when conflicts arise** or when people need to edit overlapping parts of the project.
10. **Avoid destructive commands without understanding them**, such as `git reset --hard` and `git push --force` (not covered in this workshop).
