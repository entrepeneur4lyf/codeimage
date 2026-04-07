```markdown
# codeimage Development Patterns

> Auto-generated skill from repository analysis

## Overview
This skill teaches the core development patterns and conventions used in the `codeimage` TypeScript codebase. You'll learn how to structure files, write imports and exports, follow commit message guidelines, and organize tests. These patterns help maintain consistency and readability throughout the project.

## Coding Conventions

### File Naming
- Use **camelCase** for all file names.
  - Example: `myComponent.ts`, `userProfile.test.ts`

### Import Style
- Use **relative imports** for referencing other modules.
  - Example:
    ```typescript
    import { myFunction } from './utils';
    ```

### Export Style
- Use **named exports** for all exported functions, classes, or constants.
  - Example:
    ```typescript
    // utils.ts
    export function myFunction() { ... }
    ```

### Commit Messages
- Follow **conventional commit** format.
- Use the `chore` prefix for routine changes.
  - Example:
    ```
    chore: update dependencies to latest version
    ```

## Workflows

### Commit Routine
**Trigger:** When making any code change  
**Command:** `/commit-routine`

1. Make your changes following the coding conventions.
2. Stage your changes with `git add`.
3. Write a commit message using the conventional format, usually starting with `chore:`.
   - Example: `chore: refactor file naming for consistency`
4. Commit your changes.

### Add a New Module
**Trigger:** When adding a new feature or utility  
**Command:** `/add-module`

1. Create a new file using camelCase naming (e.g., `newFeature.ts`).
2. Write your code using named exports.
3. Use relative imports to include dependencies.
4. If applicable, create a corresponding test file (e.g., `newFeature.test.ts`).

## Testing Patterns

- Test files use the `*.test.*` naming pattern.
  - Example: `myFunction.test.ts`
- The specific testing framework is not detected; follow existing patterns in the repository.
- Place tests alongside the code they test or in a dedicated test directory as per existing structure.

  ```typescript
  // myFunction.test.ts
  import { myFunction } from './myFunction';

  describe('myFunction', () => {
    it('should do something', () => {
      // test implementation
    });
  });
  ```

## Commands
| Command           | Purpose                                      |
|-------------------|----------------------------------------------|
| /commit-routine   | Guide for making a conventional commit       |
| /add-module       | Steps to add a new module with conventions   |
```
