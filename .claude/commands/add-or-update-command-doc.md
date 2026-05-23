---
name: add-or-update-command-doc
description: Workflow command scaffold for add-or-update-command-doc in linux-command.
allowed_tools: ["Bash", "Read", "Write", "Grep", "Glob"]
---

# /add-or-update-command-doc

Use this workflow when working on **add-or-update-command-doc** in `linux-command`.

## Goal

Adds a new Linux command documentation file or updates an existing one, and updates the README.md to reflect the change.

## Common Files

- `command/*.md`
- `README.md`

## Suggested Sequence

1. Understand the current state and failure mode before editing.
2. Make the smallest coherent change that satisfies the workflow goal.
3. Run the most relevant verification for touched files.
4. Summarize what changed and what still needs review.

## Typical Commit Signals

- Create or update a markdown file in command/ (e.g., command/ufw.md, command/nstat.md, command/vi.md, command/pacman.md, command/losetup.md, command/atop.md, command/git.md, command/getcap.md)
- Update README.md to mention the new or updated command

## Notes

- Treat this as a scaffold, not a hard-coded script.
- Update the command if the workflow evolves materially.