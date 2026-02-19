---
description: "{{ LOW }} Check all version number props and update them"
argument-hint: [version number]
model: haiku
---

# Version Checker

Check the following properties and update to the value show (coercing type if necessary)

- `README.md` - `# Iris v$ARGUMENTS`
- `package.json` - `"version": "$ARGUMENTS"`