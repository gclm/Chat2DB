---
name: repository-migration-or-major-release
description: Workflow command scaffold for repository-migration-or-major-release in Chat2DB.
allowed_tools: ["Bash", "Read", "Write", "Grep", "Glob"]
---

# /repository-migration-or-major-release

Use this workflow when working on **repository-migration-or-major-release** in `Chat2DB`.

## Goal

Prepares the repository for a major migration or release by removing legacy files, updating metadata, and (re)adding core source files and assets.

## Common Files

- `.github/**`
- `docker/**`
- `document/**`
- `README.md`
- `LICENSE`
- `CONTRIBUTING.md`

## Suggested Sequence

1. Understand the current state and failure mode before editing.
2. Make the smallest coherent change that satisfies the workflow goal.
3. Run the most relevant verification for touched files.
4. Summarize what changed and what still needs review.

## Typical Commit Signals

- Remove or archive legacy files and configuration (e.g., .github, docs, Docker, scripts).
- Add or update core source files and assets (e.g., src/, public/, assets/).
- Update or add project metadata and documentation (e.g., README, LICENSE, CONTRIBUTING).
- Update or add workflow and CI/CD configuration files.

## Notes

- Treat this as a scaffold, not a hard-coded script.
- Update the command if the workflow evolves materially.