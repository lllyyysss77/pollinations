---
name: add-or-update-github-workflow
description: Workflow command scaffold for add-or-update-github-workflow in pollinations.
allowed_tools: ["Bash", "Read", "Write", "Grep", "Glob"]
---

# /add-or-update-github-workflow

Use this workflow when working on **add-or-update-github-workflow** in `pollinations`.

## Goal

Adds or updates GitHub Actions workflow files to automate project tasks.

## Common Files

- `.github/workflows/*.yml`

## Suggested Sequence

1. Understand the current state and failure mode before editing.
2. Make the smallest coherent change that satisfies the workflow goal.
3. Run the most relevant verification for touched files.
4. Summarize what changed and what still needs review.

## Typical Commit Signals

- Create or modify a file in .github/workflows/.
- Commit the workflow file with a descriptive message.

## Notes

- Treat this as a scaffold, not a hard-coded script.
- Update the command if the workflow evolves materially.