---
name: git-conventions
description: Use when branching, committing, or reviewing PRs. Covers branch naming, commit message format, and PR process.
---

# Git Conventions

## Agent-managed content

This skill is maintained dynamically by agents as the project evolves.
When any agent discovers project-specific git patterns, it should update
the relevant section below:

- A different branch naming scheme (e.g., `main/`, `release/`, `hotfix/`)
- Rebase vs merge workflow preferences
- Squash merge or linear history requirements
- Signed commits or GPG requirements
- Branch protection or CI gate rules
- Specific PR template or review requirements

Do not remove content that another agent or the user has added — only
add to or refine it.

## Branch naming

| Pattern | When |
|---------|------|
| `feature/TICKETN` | New feature or enhancement |
| `bugfix/TICKETN` | Bug fix |
| `refactor/TICKETN` | Code restructuring, no behavior change |
| `docs/TICKETN` | Documentation only |
| `test/TICKETN` | Adding or fixing tests |

Always reference a ticket number when one exists.

## Commit messages

Use the project's standard format:

```
TICKETN: Brief description of the change

- Bullet summary of each logical change
- Another change
```

- **Subject**: imperative mood, <=50 chars, no trailing period
- **Body**: bullet list of specific changes for reviewer context

Examples:
```
TICKET-1: Add Retention Service

- Added new Retention Service
- Refactored existing collections by removing TTL indexes
- Updated related unit tests
```

```
TICKET-45: Fix null reference in OrderService.GetTotal

- Added null guard before accessing customer property
- Added unit test covering the edge case
```

## Workflow

- Commit message must be approved by the user.
- Do not push until commits are clean and tested.
- Do not create PRs unless explicitly asked.

## Code review

- Review the diff before committing. No debugging code, no commented-out
  code.
- Ensure no secrets, keys, or connection strings are committed.
- Ensure no `TODO`, `FIXME`, or `HACK` without a ticket reference.
