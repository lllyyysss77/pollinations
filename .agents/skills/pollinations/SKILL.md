```markdown
# pollinations Development Patterns

> Auto-generated skill from repository analysis

## Overview
This skill teaches you the core development patterns, coding conventions, and workflows used in the `pollinations` TypeScript codebase. You'll learn how to add new apps, update CI/CD workflows, develop features with proper documentation and testing, and keep your branches in sync with the main branch. The guide also covers commit style, file organization, and testing practices to help you contribute effectively.

## Coding Conventions

- **Language:** TypeScript
- **Framework:** None detected
- **File Naming:** camelCase  
  _Example:_ `appCatalog.ts`, `featureRegistry.ts`
- **Import Style:** Relative imports  
  _Example:_  
  ```ts
  import { getAppList } from './appCatalog';
  ```
- **Export Style:** Mixed (both named and default exports)  
  _Example:_  
  ```ts
  export function addApp() { ... }
  export default AppRegistry;
  ```
- **Commit Messages:**  
  - Freeform, with prefixes: `fix`, `feat`, `docs`
  - Average length: ~45 characters  
  _Examples:_  
  ```
  feat: add support for new image model
  fix: resolve API route error in app registry
  docs: update APIDOCS.md for new endpoints
  ```

## Workflows

### Add New App to Catalog
**Trigger:** When adding a new app to the Pollinations app catalog  
**Command:** `/add-app`

1. Edit `README.md` to mention the new app.
2. Edit `apps/APPS.md` to add the new app entry.
3. _Optional:_ Update `enter.pollinations.ai/package-lock.json` if dependencies change.
4. Commit changes with a descriptive message.

_Example commit message:_  
```
feat: add "DreamPainter" app to catalog
```

---

### Add or Update GitHub Workflow
**Trigger:** When introducing or modifying CI/CD or automation workflows  
**Command:** `/add-workflow`

1. Create or modify a file in `.github/workflows/` (YAML format).
2. Commit the workflow file with a descriptive message.

_Example:_  
Create `.github/workflows/deploy.yml`  
```yaml
name: Deploy
on: [push]
jobs:
  deploy:
    runs-on: ubuntu-latest
    steps:
      - uses: actions/checkout@v2
      # ... more steps
```
_Example commit message:_  
```
feat: add deploy workflow for continuous deployment
```

---

### Feature Development with API and Docs
**Trigger:** When adding a new model, endpoint, or major backend feature  
**Command:** `/add-feature`

1. Edit or add API route files in `enter.pollinations.ai/src/routes/`.
2. Update shared registries in `shared/registry/`.
3. Write or update integration tests in `enter.pollinations.ai/test/integration/`.
4. Update documentation, such as `APIDOCS.md` or client component data files.
5. Commit all related changes.

_Example:_  
```ts
// enter.pollinations.ai/src/routes/newModel.ts
export function newModelHandler(req, res) {
  // implementation
}
```
_Example commit message:_  
```
feat: add newModel API route and docs
```

---

### Merge Main into Feature Branch
**Trigger:** When syncing a feature branch with the latest main branch changes  
**Command:** `/merge-main`

1. Merge `main` into your feature branch.
2. Resolve any merge conflicts across affected files and directories.
3. Commit all updated files, including workflows, docs, scripts, and source code.

_Example:_  
```
git checkout feature/my-feature
git merge main
# resolve conflicts
git add .
git commit -m "chore: merge main into feature/my-feature"
```

## Testing Patterns

- **Test Framework:** Unknown (likely Jest or similar for TypeScript)
- **Test File Pattern:** `*.test.ts`
- **Location:** Typically in `enter.pollinations.ai/test/integration/`
- **Example Test File:**
  ```ts
  // enter.pollinations.ai/test/integration/newModel.test.ts
  import { newModelHandler } from '../../src/routes/newModel';

  test('newModelHandler returns 200', () => {
    // test implementation
  });
  ```

## Commands

| Command      | Purpose                                                      |
|--------------|--------------------------------------------------------------|
| /add-app     | Add a new app to the catalog and update documentation        |
| /add-workflow| Add or update a GitHub Actions workflow                      |
| /add-feature | Implement a new feature, including API, tests, and docs      |
| /merge-main  | Merge main branch into a feature branch and resolve conflicts |
```
