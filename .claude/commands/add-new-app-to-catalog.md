---
name: add-new-app-to-catalog
description: Workflow command scaffold for add-new-app-to-catalog in pollinations.
allowed_tools: ["Bash", "Read", "Write", "Grep", "Glob"]
---

# /add-new-app-to-catalog

Use this workflow when working on **add-new-app-to-catalog** in `pollinations`.

## Goal

Adds a new app to the Pollinations app catalog, updating documentation and app listings.

## Common Files

- `README.md`
- `apps/APPS.md`
- `enter.pollinations.ai/package-lock.json`

## Suggested Sequence

1. Understand the current state and failure mode before editing.
2. Make the smallest coherent change that satisfies the workflow goal.
3. Run the most relevant verification for touched files.
4. Summarize what changed and what still needs review.

## Typical Commit Signals

- Edit README.md to mention the new app.
- Edit apps/APPS.md to add the new app entry.
- Optionally update enter.pollinations.ai/package-lock.json if dependencies are involved.

## Notes

- Treat this as a scaffold, not a hard-coded script.
- Update the command if the workflow evolves materially.