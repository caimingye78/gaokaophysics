```markdown
# gaokaophysics Development Patterns

> Auto-generated skill from repository analysis

## Overview
This skill teaches you the core development patterns and conventions used in the `gaokaophysics` TypeScript codebase. You'll learn how to structure files, write and organize code, follow commit conventions, and implement and run tests in a consistent manner. This guide is designed to help contributors maintain code quality and consistency across the project.

## Coding Conventions

### File Naming
- Use **camelCase** for all file names.
  - Example: `physicsUtils.ts`, `calculateScore.ts`

### Import Style
- Use **relative imports** for all modules.
  - Example:
    ```typescript
    import { calculateScore } from './calculateScore';
    ```

### Export Style
- Use **named exports**.
  - Example:
    ```typescript
    // In calculateScore.ts
    export function calculateScore() { ... }
    ```

### Commit Messages
- Follow the **conventional commit** format.
- Use the `feat` prefix for new features.
  - Example:
    ```
    feat: add support for new physics formula
    ```

## Workflows

### Feature Development
**Trigger:** When adding a new feature or module  
**Command:** `/feature-development`

1. Create a new file using camelCase naming.
2. Write your TypeScript code using named exports.
3. Use relative imports to include dependencies.
4. Write corresponding test files using the `*.test.*` pattern.
5. Commit your changes using the conventional commit format (`feat: ...`).
6. Submit a pull request for review.

### Testing
**Trigger:** When verifying code correctness  
**Command:** `/run-tests`

1. Identify or create test files matching the `*.test.*` pattern.
2. Use the project's preferred testing framework (unknown; refer to project documentation or existing tests).
3. Run all test files to ensure code passes.
4. Address any test failures before merging.

## Testing Patterns

- Test files follow the `*.test.*` naming pattern (e.g., `calculateScore.test.ts`).
- The testing framework is not specified; review existing test files for structure and assertions.
- Place test files alongside or near the modules they test.

**Example test file:**
```typescript
import { calculateScore } from './calculateScore';

test('calculates score correctly', () => {
  expect(calculateScore(5, 10)).toBe(50);
});
```

## Commands
| Command              | Purpose                                      |
|----------------------|----------------------------------------------|
| /feature-development | Start the workflow for adding new features   |
| /run-tests           | Run all test files to verify code correctness|
```
