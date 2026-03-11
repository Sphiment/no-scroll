# CLAUDE.md

This file provides guidance to AI assistants (Claude and others) working on the `no-scroll` repository.

## Project Overview

**Repository:** `Sphiment/no-scroll`
**License:** GNU General Public License v3 (GPLv3)
**Status:** Early initialization — no source code yet.

The project is named `no-scroll` and is currently at its very first commit (only a LICENSE file is present). All technology stack choices, source structure, and conventions will be established as the project develops.

## Current Repository State

```
no-scroll/
├── .git/
├── LICENSE     ← GNU GPL v3
└── CLAUDE.md   ← this file
```

No source code, build configuration, test framework, or tooling has been set up yet.

## Git Workflow

### Branching Convention

- Feature/task branches created by Claude follow the pattern: `claude/<task-id>`
- The main branch is `master`
- Never push directly to `master` without explicit user permission

### Commit Messages

- Use imperative mood: "Add feature" not "Added feature"
- Keep the subject line under 72 characters
- Reference issue numbers when applicable: `Fix crash on load (#42)`

### Push Instructions

Always push with upstream tracking:

```bash
git push -u origin <branch-name>
```

Only retry on network failures (up to 4 times with exponential backoff: 2s, 4s, 8s, 16s).

## Development Guidelines (to be updated as the project grows)

Since the project has no source code yet, the following are placeholder conventions to fill in once the stack is chosen:

### Adding New Code

- Keep files focused and single-purpose
- Prefer editing existing files over creating new ones
- Avoid over-engineering; implement only what the current task requires

### Testing

- Add tests alongside new features as the testing framework is established
- Run the test suite before committing

### Linting / Formatting

- Formatting and linting tooling to be determined
- Once configured, run linters before committing

## Notes for AI Assistants

- **Read before writing.** Always read existing files before proposing or making changes.
- **Minimal changes.** Only change what is directly required by the task. Do not refactor unrelated code or add unrequested documentation/comments.
- **Verify assumptions.** If the technology stack or conventions are unclear, ask the user rather than guessing.
- **Security.** Never introduce OWASP top-10 vulnerabilities (XSS, SQL injection, command injection, etc.).
- **No backwards-compat hacks.** If something is unused, remove it cleanly rather than leaving dead code behind.
- **This file is living documentation.** Update CLAUDE.md whenever significant structural or workflow changes are made to the repository.
