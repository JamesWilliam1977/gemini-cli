---
name: documentation-update
description: Workflow command scaffold for documentation-update in gemini-cli.
allowed_tools: ["Bash", "Read", "Write", "Grep", "Glob"]
---

# /documentation-update

Use this workflow when working on **documentation-update** in `gemini-cli`.

## Goal

Updates or adds documentation files, often across multiple related docs, sometimes updating sidebar or changelog.

## Common Files

- `docs/cli/creating-skills.md`
- `docs/cli/skills-best-practices.md`
- `docs/cli/skills.md`
- `docs/cli/tutorials/skills-getting-started.md`
- `docs/cli/using-agent-skills.md`
- `docs/tools/activate-skill.md`

## Suggested Sequence

1. Understand the current state and failure mode before editing.
2. Make the smallest coherent change that satisfies the workflow goal.
3. Run the most relevant verification for touched files.
4. Summarize what changed and what still needs review.

## Typical Commit Signals

- Edit or add documentation markdown files (e.g., docs/cli/*.md, docs/tools/*.md).
- Optionally update sidebar or changelog files (e.g., docs/sidebar.json, docs/changelogs/latest.md).

## Notes

- Treat this as a scaffold, not a hard-coded script.
- Update the command if the workflow evolves materially.