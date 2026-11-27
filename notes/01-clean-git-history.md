# Keeping a clean Git history

A readable history makes reviews, debugging, and releases easier. The goal is not a perfect graph; it is a sequence of commits that each explain one change.

## Key practices

- Commit one logical change at a time. Keep refactors separate from behavior changes.
- Write the subject in the imperative mood and keep it under about 72 characters.
- Use the body to explain why the change is needed; the diff already shows what changed.
- Rebase local branches before opening a pull request to remove temporary commits.
- Do not rewrite shared history without coordinating with everyone who uses the branch.

## Why it matters

When a bug appears months later, a clean history lets you bisect and revert with confidence.

