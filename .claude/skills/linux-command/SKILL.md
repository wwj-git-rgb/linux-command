```markdown
# linux-command Development Patterns

> Auto-generated skill from repository analysis

## Overview

This skill introduces the development patterns and workflows used in the `linux-command` TypeScript repository. The project focuses on documenting Linux commands, maintaining up-to-date documentation, and acknowledging contributors. You'll learn about the code style, file organization, and the step-by-step processes for updating documentation and contributor information.

## Coding Conventions

- **Language:** TypeScript (no framework)
- **File Naming:** Use camelCase for all files.
  - Example: `getCap.ts`, `linuxCommandParser.ts`
- **Import Style:** Use relative imports.
  - Example:
    ```typescript
    import { parseCommand } from './parseCommand'
    ```
- **Export Style:** Use named exports.
  - Example:
    ```typescript
    export function parseCommand() { ... }
    ```
- **Commit Messages:** Freeform, with occasional prefixes like `doc` and `feat`.
  - Example: `doc: add ufw command documentation`
- **Documentation Files:** Each Linux command has its own markdown file in the `command/` directory.
  - Example: `command/ufw.md`

## Workflows

### Add or Update Command Documentation
**Trigger:** When you want to add documentation for a new Linux command or update an existing command's documentation.  
**Command:** `/add-command-doc`

1. Create or update a markdown file in the `command/` directory.
   - Example: `command/vi.md`
2. Update `README.md` to mention the new or updated command.
3. Commit your changes with a descriptive message.
   - Example: `doc: add vi command documentation`

**Example:**
```bash
# Add new documentation
echo "# vi" > command/vi.md

# Update README
echo "- [vi](command/vi.md)" >> README.md

git add command/vi.md README.md
git commit -m "doc: add vi command documentation"
git push
```

---

### Update README and Contributors
**Trigger:** When you want to update project metadata, acknowledge contributors, or reflect new changes in documentation.  
**Command:** `/update-readme-contributors`

1. Edit `README.md` as needed.
2. Edit `template/contributors.ejs` to add or update contributors.
3. Commit your changes.
   - Example: `doc: update contributors list`

**Example:**
```bash
# Edit README.md and template/contributors.ejs
git add README.md template/contributors.ejs
git commit -m "doc: update contributors list"
git push
```

---

### Update README Only
**Trigger:** When you want to make a minor documentation update or fix in the `README.md`.  
**Command:** `/update-readme`

1. Edit `README.md`.
2. Commit your changes.
   - Example: `doc: fix typo in README`

**Example:**
```bash
# Edit README.md
git add README.md
git commit -m "doc: fix typo in README"
git push
```

---

### Update Contributors Template Only
**Trigger:** When you want to update the contributors list or page layout without touching other files.  
**Command:** `/update-contributors-template`

1. Edit `template/contributors.ejs`.
2. Commit your changes.
   - Example: `doc: update contributors template`

**Example:**
```bash
# Edit template/contributors.ejs
git add template/contributors.ejs
git commit -m "doc: update contributors template"
git push
```

## Testing Patterns

- **Test Files:** Use the pattern `*.test.*` for test files.
  - Example: `parseCommand.test.ts`
- **Testing Framework:** Not explicitly specified; check existing test files for conventions.
- **Typical Test Example:**
  ```typescript
  import { parseCommand } from './parseCommand'

  describe('parseCommand', () => {
    it('parses a basic command', () => {
      expect(parseCommand('ls -l')).toEqual({ command: 'ls', options: ['-l'] })
    })
  })
  ```

## Commands

| Command                        | Purpose                                                      |
|---------------------------------|--------------------------------------------------------------|
| /add-command-doc                | Add or update a Linux command documentation file             |
| /update-readme-contributors     | Update README and contributors template                      |
| /update-readme                  | Update README.md only                                        |
| /update-contributors-template   | Update contributors template only                            |
```
