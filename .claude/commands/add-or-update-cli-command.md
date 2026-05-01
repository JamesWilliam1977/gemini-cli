---
name: add-or-update-cli-command
description: Workflow command scaffold for add-or-update-cli-command in gemini-cli.
allowed_tools: ["Bash", "Read", "Write", "Grep", "Glob"]
---

# /add-or-update-cli-command

Use this workflow when working on **add-or-update-cli-command** in `gemini-cli`.

## Goal

Adds a new CLI command or updates an existing one, updating the command implementation, its tests, and related documentation.

## Common Files

- `packages/cli/src/ui/commands/commandsCommand.ts`
- `packages/cli/src/ui/commands/commandsCommand.test.ts`
- `packages/cli/src/ui/commands/__snapshots__/commandsCommand.test.ts.snap`
- `docs/cli/cli-reference.md`
- `docs/cli/custom-commands.md`
- `docs/reference/commands.md`

## Suggested Sequence

1. Understand the current state and failure mode before editing.
2. Make the smallest coherent change that satisfies the workflow goal.
3. Run the most relevant verification for touched files.
4. Summarize what changed and what still needs review.

## Typical Commit Signals

- Edit or create the command implementation file (e.g., commandsCommand.ts).
- Edit or create the corresponding test file (e.g., commandsCommand.test.ts).
- Update documentation files describing the command (e.g., docs/cli/cli-reference.md, docs/reference/commands.md).
- Update snapshot files if present.

## Notes

- Treat this as a scaffold, not a hard-coded script.
- Update the command if the workflow evolves materially.