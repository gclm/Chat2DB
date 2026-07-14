```markdown
# Chat2DB Development Patterns

> Auto-generated skill from repository analysis

## Overview
This skill teaches the core development patterns, coding conventions, and repository workflows for the Chat2DB project. The codebase is written in TypeScript and follows consistent conventions for file naming, imports, exports, and commit messages. This guide will help you contribute effectively, maintain code quality, and follow established workflows for major releases or migrations.

## Coding Conventions

### File Naming
- Use **camelCase** for file names.
  - Example: `userService.ts`, `chatManager.test.ts`

### Import Style
- Use **relative imports** for internal modules.
  - Example:
    ```typescript
    import { fetchData } from './apiClient';
    ```

### Export Style
- Use **named exports** rather than default exports.
  - Example:
    ```typescript
    // In userService.ts
    export function getUser(id: string) { ... }
    export const USER_ROLE = 'admin';
    ```

### Commit Messages
- Follow **conventional commit** format.
- Common prefixes: `chore`, `feat`
- Example:
  ```
  feat: add support for new database driver
  chore: update dependencies and fix lint errors
  ```

## Workflows

### Repository Migration or Major Release
**Trigger:** When preparing for a major community migration or a new major release.  
**Command:** `/prepare-migration`

1. **Remove or archive legacy files and configuration**
   - Delete or move outdated files and folders such as `.github/`, `docker/`, `document/`, and any legacy scripts.
2. **Add or update core source files and assets**
   - Ensure the latest versions of `src/`, `public/`, `assets/`, and `chat2db-client/` are present and up to date.
3. **Update or add project metadata and documentation**
   - Review and update `README.md`, `LICENSE`, `CONTRIBUTING.md`, and `CHANGELOG.md` to reflect the latest changes.
4. **Update or add workflow and CI/CD configuration files**
   - Make sure all workflow files (e.g., GitHub Actions, CI/CD configs) are current and relevant to the new release or migration.

**Example Directory Changes:**
```
- Remove: .github/old-workflows.yml
- Update: README.md with new features
- Add: src/newFeature.ts
```

## Testing Patterns

- Test files use the `.test.ts` suffix.
  - Example: `userService.test.ts`
- Testing framework is **unknown**; check existing test files for patterns.
- Example test file structure:
  ```typescript
  import { getUser } from './userService';

  describe('getUser', () => {
    it('returns user data for valid id', () => {
      // test implementation
    });
  });
  ```

## Commands
| Command            | Purpose                                                        |
|--------------------|----------------------------------------------------------------|
| /prepare-migration | Prepare the repository for a major migration or new release    |
```
