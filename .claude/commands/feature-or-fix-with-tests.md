---
name: feature-or-fix-with-tests
description: Workflow command scaffold for feature-or-fix-with-tests in gemini-cli.
allowed_tools: ["Bash", "Read", "Write", "Grep", "Glob"]
---

# /feature-or-fix-with-tests

Use this workflow when working on **feature-or-fix-with-tests** in `gemini-cli`.

## Goal

Implements a new feature or fixes a bug, always updating both implementation and corresponding test files.

## Common Files

- `packages/cli/src/ui/components/InputPrompt.tsx`
- `packages/cli/src/ui/components/InputPrompt.test.tsx`
- `packages/cli/src/utils/sessionCleanup.ts`
- `packages/cli/src/utils/sessionCleanup.test.ts`
- `packages/core/src/services/chatRecordingService.ts`
- `packages/core/src/services/chatRecordingService.test.ts`

## Suggested Sequence

1. Understand the current state and failure mode before editing.
2. Make the smallest coherent change that satisfies the workflow goal.
3. Run the most relevant verification for touched files.
4. Summarize what changed and what still needs review.

## Typical Commit Signals

- Edit or create the implementation file (e.g., .ts or .tsx).
- Edit or create the corresponding test file (e.g., .test.ts or .test.tsx).

## Notes

- Treat this as a scaffold, not a hard-coded script.
- Update the command if the workflow evolves materially.