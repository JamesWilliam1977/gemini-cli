```markdown
# gemini-cli Development Patterns

> Auto-generated skill from repository analysis

## Overview

This skill teaches you how to contribute to the `gemini-cli` TypeScript codebase, which provides a command-line interface for interacting with Gemini. You'll learn the project's coding conventions, how to add features or fix bugs with tests, how to add or update CLI commands with documentation, and how to update documentation effectively. The repository uses conventional commits, a clear file structure, and emphasizes test coverage and documentation.

## Coding Conventions

- **File Naming:**  
  Use `camelCase` for files and directories.  
  _Example:_  
  ```
  packages/cli/src/utils/sessionCleanup.ts
  packages/core/src/services/chatRecordingService.ts
  ```

- **Import Style:**  
  Use **relative imports** for internal modules.  
  _Example:_  
  ```typescript
  import { sessionCleanup } from '../utils/sessionCleanup';
  ```

- **Export Style:**  
  Use **named exports**.  
  _Example:_  
  ```typescript
  // sessionCleanup.ts
  export function sessionCleanup() { ... }
  ```

- **Commit Messages:**  
  Follow **conventional commit** style with prefixes like `fix`, `feat`, `docs`, `test`.  
  _Example:_  
  ```
  feat: add session cleanup utility for expired sessions
  fix: correct prompt rendering in InputPrompt component
  ```

## Workflows

### Feature or Fix with Tests
**Trigger:** When you add a new feature or fix a bug and need to ensure it's tested  
**Command:** `/feature-with-tests`

1. **Edit or create the implementation file**  
   _Example:_  
   ```
   packages/cli/src/utils/sessionCleanup.ts
   ```
2. **Edit or create the corresponding test file**  
   _Example:_  
   ```
   packages/cli/src/utils/sessionCleanup.test.ts
   ```
3. **Commit with a conventional message**  
   _Example:_  
   ```
   feat: implement session cleanup and add tests
   ```
4. **Run tests to verify correctness**  
   ```
   npx vitest
   ```

---

### Add or Update CLI Command
**Trigger:** When you want to add a new CLI command or update an existing one, including tests and docs  
**Command:** `/new-cli-command`

1. **Edit or create the command implementation file**  
   _Example:_  
   ```
   packages/cli/src/ui/commands/commandsCommand.ts
   ```
2. **Edit or create the corresponding test file**  
   _Example:_  
   ```
   packages/cli/src/ui/commands/commandsCommand.test.ts
   ```
3. **Update documentation files**  
   _Examples:_  
   ```
   docs/cli/cli-reference.md
   docs/cli/custom-commands.md
   docs/reference/commands.md
   ```
4. **Update snapshot files if present**  
   _Example:_  
   ```
   packages/cli/src/ui/commands/__snapshots__/commandsCommand.test.ts.snap
   ```
5. **Commit with a descriptive message**  
   ```
   feat: add new 'commands' CLI command with docs and tests
   ```

---

### Documentation Update
**Trigger:** When you want to add, update, or improve documentation  
**Command:** `/update-docs`

1. **Edit or add documentation markdown files**  
   _Examples:_  
   ```
   docs/cli/creating-skills.md
   docs/cli/skills-best-practices.md
   docs/cli/tutorials/skills-getting-started.md
   docs/tools/activate-skill.md
   ```
2. **Optionally update sidebar or changelog files**  
   _Examples:_  
   ```
   docs/sidebar.json
   docs/changelogs/latest.md
   ```
3. **Commit with a `docs:` prefix**  
   ```
   docs: update skills best practices and sidebar
   ```

## Testing Patterns

- **Framework:** [vitest](https://vitest.dev/)
- **Test File Pattern:**  
  Test files are named with `.test.ts` or `.test.tsx` and placed alongside implementation files.
  ```
  packages/cli/src/utils/sessionCleanup.test.ts
  packages/cli/src/ui/components/InputPrompt.test.tsx
  ```
- **Example Test:**
  ```typescript
  import { describe, it, expect } from 'vitest';
  import { sessionCleanup } from './sessionCleanup';

  describe('sessionCleanup', () => {
    it('removes expired sessions', () => {
      // test logic here
      expect(sessionCleanup(...)).toBe(...);
    });
  });
  ```

## Commands

| Command              | Purpose                                                        |
|----------------------|----------------------------------------------------------------|
| /feature-with-tests  | Add a new feature or fix a bug, always with corresponding tests|
| /new-cli-command     | Add or update a CLI command, including tests and documentation |
| /update-docs         | Update or add documentation files                              |
```
