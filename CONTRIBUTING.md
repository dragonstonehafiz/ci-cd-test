# Contributing Guidelines

Thanks for contributing! This document covers the conventions this project follows.

## Branch Naming

Branches must be named `<type>/<description>`, where `<type>` is one of:

- `feature/` — new features or enhancements
- `bugfix/` — bug fixes
- `hotfix/` — production hotfixes
- `release/` — release branches (e.g. `release/v1.2.0`)

Examples: `feature/user-authentication`, `bugfix/fix-login-timeout`, `hotfix/critical-security-patch`.

Invalid: `my-feature`, `fix/bug`, `feature-branch` (no slash), `add-authentication` (no type prefix).

## Commit Messages

Commits must follow [Conventional Commits](https://www.conventionalcommits.org/en/v1.0.0/):

```
<type>(<optional-scope>): <description>
```

Types: `feat`, `fix`, `docs`, `style`, `refactor`, `perf`, `test`, `build`, `ci`, `chore`, `revert`.

Add `!` after the type/scope for breaking changes, e.g. `feat(api)!: change auth method`.

Examples:

```
feat: add user authentication
fix(api): handle null response from backend
docs: update installation instructions
ci: add automated deployment workflow
```

### Enforcement

This repo has a commit-msg hook under `.github/hooks/commit-msg` that checks the format above. Install it with:

```bash
git config core.hooksPath .github/hooks
```

## Pull Requests

1. Push your branch and open a PR against `main`.
2. Request review from at least one other developer.
3. Make sure all automated checks pass before merging.

PR titles should also follow Conventional Commits format.

## Local Development Setup

```bash
git clone <repository-url>
cd <repository-name>
git config core.hooksPath .github/hooks
git checkout -b feature/your-feature-name
```
