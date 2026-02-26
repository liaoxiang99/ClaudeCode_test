# CLAUDE.md

This file provides guidance to AI assistants (Claude and others) working with this repository.

## Repository Overview

**Repository:** `liaoxiang99/ClaudeCode_test`
**Status:** Newly initialized — no source code has been added yet.

This document will be updated as the project grows. The sections below establish conventions and workflows that should be followed from the start.

---

## Repository Structure

```
ClaudeCode_test/
├── CLAUDE.md          # This file — AI assistant guidance
└── (project files to be added)
```

As the codebase evolves, update this tree to reflect the actual structure.

---

## Git Workflow

### Branching Convention

- **Main branch:** `main` (or `master`) — stable, production-ready code only
- **Feature branches:** `feature/<short-description>`
- **Bug fix branches:** `fix/<short-description>`
- **Claude AI branches:** `claude/<task-id>` — used by AI-assisted sessions

### Commit Messages

Follow the [Conventional Commits](https://www.conventionalcommits.org/) format:

```
<type>(<scope>): <short summary>

[optional body]

[optional footer]
```

**Types:**
- `feat` — new feature
- `fix` — bug fix
- `docs` — documentation only
- `style` — formatting, whitespace (no logic change)
- `refactor` — code restructuring (no feature/fix)
- `test` — adding or updating tests
- `chore` — build process, dependency updates, tooling

**Examples:**
```
feat(auth): add JWT token refresh logic
fix(api): handle null response from user endpoint
docs: update README with setup instructions
```

### Push Workflow

```bash
# Create and switch to a new branch
git checkout -b feature/my-feature

# Stage and commit changes
git add <files>
git commit -m "feat: add my feature"

# Push with upstream tracking
git push -u origin feature/my-feature
```

---

## Development Setup

> To be filled in once the project stack is decided. Include:
> - Runtime/language version requirements
> - Dependency installation command
> - Environment variable setup (`.env.example`)
> - Database/service setup steps

### Quick Start (template)

```bash
# 1. Clone the repository
git clone <repo-url>
cd ClaudeCode_test

# 2. Install dependencies
# (add command here, e.g. npm install / pip install -r requirements.txt)

# 3. Copy environment config
cp .env.example .env
# Edit .env with your local values

# 4. Start development server
# (add command here)
```

---

## Running Tests

> To be filled in once the test framework is chosen.

```bash
# Run all tests
# (add command here, e.g. npm test / pytest / go test ./...)

# Run tests in watch mode
# (add command here)

# Run a single test file
# (add command here)
```

**Conventions:**
- All tests live in a `tests/` or `__tests__/` directory mirroring the source tree
- Test files follow the naming pattern `*.test.<ext>` or `*_test.<ext>`
- Every pull request must pass all tests before merging

---

## Code Style & Linting

> To be filled in once linting tools are configured.

- Formatter: (e.g., Prettier, Black, gofmt)
- Linter: (e.g., ESLint, Flake8, golangci-lint)
- Run linting: `(add command here)`
- Auto-fix: `(add command here)`

**General principles:**
- Keep functions small and single-purpose
- Prefer explicit over implicit
- Write self-documenting code; add comments only where logic is non-obvious
- Avoid over-engineering — solve the problem at hand, not hypothetical future ones

---

## Environment Variables

> Document required environment variables here as they are added.

| Variable | Required | Description | Example |
|----------|----------|-------------|---------|
| (none yet) | — | — | — |

Never commit `.env` files or secrets. Use `.env.example` to document required variables with placeholder values.

---

## AI Assistant Guidelines

When working in this repository as an AI assistant:

### Do

- Read existing files before modifying them
- Follow the commit message convention above
- Keep changes minimal and focused on the task
- Write tests for new logic
- Update this CLAUDE.md when project structure or conventions change
- Use the branch `claude/<task-id>` for AI-assisted work and push there

### Do Not

- Push directly to `main`/`master`
- Commit secrets, credentials, or `.env` files
- Add unnecessary dependencies
- Refactor code that is outside the scope of the current task
- Leave TODO comments without a linked issue or explanation

### Branch & Push Instructions for Claude Sessions

```bash
# Ensure you are on the correct claude branch
git checkout claude/<session-branch-name>

# After making changes, commit and push
git add CLAUDE.md   # or specific files
git commit -m "docs: add/update CLAUDE.md"
git push -u origin claude/<session-branch-name>
```

---

## Pull Request Checklist

Before opening a PR:

- [ ] All tests pass
- [ ] Linting passes with no errors
- [ ] New features have test coverage
- [ ] CLAUDE.md updated if project structure changed
- [ ] Commit messages follow the convention above
- [ ] No secrets or sensitive data committed

---

## Contact & Ownership

- **Repository owner:** `liaoxiang99`
- **Issue tracker:** (link to issues page)
- **Main branch protection:** PRs require review before merging

---

*Last updated: 2026-02-26 — Initial CLAUDE.md creation for empty repository.*
