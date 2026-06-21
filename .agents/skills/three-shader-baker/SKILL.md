```markdown
# three-shader-baker Development Patterns

> Auto-generated skill from repository analysis

## Overview
This skill teaches you the core development patterns and conventions used in the `three-shader-baker` TypeScript codebase. You'll learn how to structure files, write imports and exports, and follow the project's testing and workflow conventions. This guide is ideal for contributors who want to maintain consistency and quality in their code contributions.

## Coding Conventions

### File Naming
- Use **camelCase** for file names.
  - Example: `shaderUtils.ts`, `bakeShader.test.ts`

### Import Style
- Use **relative imports** for modules within the project.
  - Example:
    ```typescript
    import { bakeShader } from './bakeShader';
    ```

### Export Style
- Use **named exports** for functions, classes, and constants.
  - Example:
    ```typescript
    export function bakeShader() { ... }
    export const SHADER_VERSION = 2;
    ```

### Commit Messages
- Freeform style, no enforced prefixes.
- Average commit message length is about 64 characters.
  - Example:
    ```
    Add initial shader baking utility and basic tests
    ```

## Workflows

### Adding a New Utility Module
**Trigger:** When you need to add a new helper or utility function.
**Command:** `/add-utility-module`

1. Create a new TypeScript file using camelCase (e.g., `myUtility.ts`).
2. Write your function(s) and export them using named exports.
    ```typescript
    export function myUtility() { ... }
    ```
3. Import your utility in other files using a relative path.
    ```typescript
    import { myUtility } from './myUtility';
    ```
4. Write a corresponding test file named `myUtility.test.ts`.

### Writing and Running Tests
**Trigger:** When you add or modify code and need to verify correctness.
**Command:** `/run-tests`

1. Create a test file with the pattern `*.test.ts` (e.g., `bakeShader.test.ts`).
2. Write your tests using the project's preferred (unknown) testing framework.
3. Run the test suite using the project's test runner (see project documentation for details).

### Making a Commit
**Trigger:** After making code changes.
**Command:** `/commit-changes`

1. Stage your changes using git.
2. Write a clear, descriptive commit message (no specific prefix required).
    ```
    Fix shader parameter handling in bakeShader
    ```
3. Commit your changes.

## Testing Patterns

- Test files are named with the pattern `*.test.ts`.
- The specific testing framework is not detected; follow existing test file patterns.
- Place tests alongside or near the code they test.
- Example test file name: `bakeShader.test.ts`

## Commands
| Command              | Purpose                                      |
|----------------------|----------------------------------------------|
| /add-utility-module  | Scaffold a new utility module file           |
| /run-tests           | Run the project's test suite                 |
| /commit-changes      | Commit your staged changes with a message    |
```
