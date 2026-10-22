# Development Guide

How we branch, merge, and commit. Read this before opening your first PR.

## Branching Strategy

Two long-lived branches:

- `main`: production-ready code. Only receives merges from `dev`.
- `dev`: integration branch. All work lands here first.

All work happens on short-lived branches cut from `dev`, named `<category>/<category>-<number>`:

- `feature/feat-1`
- `patch/patch-1`
- `<category>/<category>-<number>` for any other kind of work

Keep branches **byte-sized**: one branch, one small focused change. If it's growing, split it.

## Deployment Flow

1. Open a PR from your branch into `dev`. **At least 3 approving reviews** required.
2. Once `dev` is stable, open a PR from `dev` into `main`. Again, **3 reviews** required.

```
feature/feat-1  ─┐
patch/patch-1   ─┼──▶  dev  ──▶  main
<category>/...  ─┘   (3 reviews)  (3 reviews)
```

## Merging Strategy

| Merge | Method |
| ----- | ------ |
| Branch → `dev` | **Squash and merge** |
| `dev` → `main` | **Merge commit** (no squash, no rebase) |

The squashed commit message must follow Conventional Commits, so write your PR title accordingly.

## Commit Conventions

We follow [Conventional Commits](https://www.conventionalcommits.org/en/v1.0.0/).

```
<type>(<optional scope>): <short description>
```

Common types: `feat`, `fix`, `docs`, `style`, `refactor`, `test`, `chore`.

```
feat(auth): add password reset flow
fix(api): handle null response from user endpoint
```

Mark breaking changes with `!`, e.g. `feat(api)!: remove v1 endpoints`.

## Good Practices

- **Test your code.** Ship tests with your changes.
- **Review others' PRs.** Don't leave them waiting. Check that the change matches the task and fits our conventions.
- **Use the enforced linting tools.** Run them before pushing. Don't bypass them.
- **Keep PRs small and well described.** Say what changed and why.
- **Stay up to date.** Sync with `dev` regularly to avoid nasty conflicts.
- **No secrets in commits.** Use environment variables.
- **Delete merged branches.**
