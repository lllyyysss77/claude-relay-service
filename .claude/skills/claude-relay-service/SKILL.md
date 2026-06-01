```markdown
# claude-relay-service Development Patterns

> Auto-generated skill from repository analysis

## Overview
This skill introduces the core development patterns and workflows used in the `claude-relay-service` JavaScript codebase. It covers coding conventions, file organization, testing strategies, and step-by-step guides for common development workflows, ensuring consistency and reliability across contributions.

## Coding Conventions

### File Naming
- Use **camelCase** for file names.
  - Example: `unifiedOpenAIScheduler.js`

### Import Style
- Use **relative imports** for modules within the project.
  - Example:
    ```javascript
    import { scheduleTask } from './taskScheduler';
    ```

### Export Style
- Use **named exports**.
  - Example:
    ```javascript
    // In unifiedOpenAIScheduler.js
    export function unifiedOpenAIScheduler(config) {
      // implementation
    }
    ```

### Commit Messages
- Prefix commits with the type of change, such as `fix:` or `chore:`.
- Keep commit messages concise (average ~62 characters).
  - Example: `fix: handle edge case in unifiedOpenAIScheduler`

## Workflows

### Feature or Bugfix with Test
**Trigger:** When adding a new feature or fixing a bug in a scheduler/service and ensuring it is tested  
**Command:** `/feature-with-test`

1. **Modify or add logic** in a service file under `src/services/scheduler/`.
   - Example: Edit `src/services/scheduler/unifiedOpenAIScheduler.js`
2. **Update or add the corresponding test file** under `tests/`.
   - Example: Edit or create `tests/unifiedOpenAIScheduler.test.js`
3. **Follow coding conventions** for file naming, imports, and exports.
4. **Commit your changes** with an appropriate prefix (`fix:`, `chore:`).
5. **Run tests** to ensure coverage for the new or updated logic.

#### Example
```javascript
// src/services/scheduler/unifiedOpenAIScheduler.js
export function unifiedOpenAIScheduler(config) {
  // New or updated logic here
}
```
```javascript
// tests/unifiedOpenAIScheduler.test.js
import { unifiedOpenAIScheduler } from '../src/services/scheduler/unifiedOpenAIScheduler';

test('should schedule tasks correctly', () => {
  // Test implementation
});
```

## Testing Patterns

- **Test files** are placed in the `tests/` directory.
- **Naming convention:** Match the source file with `.test.js` suffix.
  - Example: `unifiedOpenAIScheduler.test.js` tests `unifiedOpenAIScheduler.js`
- **Testing framework:** Not explicitly specified; use standard JavaScript testing patterns.
- **Test structure:** Use descriptive test names and cover all new/modified logic.

## Commands

| Command             | Purpose                                                      |
|---------------------|--------------------------------------------------------------|
| /feature-with-test  | Scaffold a feature or bugfix along with corresponding tests. |
```
