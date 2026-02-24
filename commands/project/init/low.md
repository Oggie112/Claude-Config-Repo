---
description: "{{ LOW }} Initialize a new project from the Kamino template"
model: haiku
---

<overview>
  Gather project details conversationally, then configure all template files.
</overview>
<read-templates>
  Read ~/.claude/library/templates/ to understand target file structure before asking questions.
  The "Before" section of each file is the canonical template; "After" shows expected output for a real project:
  - CLAUDE.md       → .claude/CLAUDE.md
  - Readme.md       → docs/README.md
  - Mvp.md          → docs/roadmaps/mvp.md
  - mcp.json.md     → .claude/.mcp.json
  - Adr.md          → docs/adrs/README.md (ADR index)
  - adr-entry.md    → docs/adrs/001-initial-tech-stack.md (first ADR entry)
</read-templates>
<gather-info>
  Ask one at a time:
  1. Project name
  2. Description (1-2 sentences)
  3. Tech stack (e.g., "SvelteKit + TypeScript", "Tauri + Svelte")
  4. Package manager (npm/bun/pnpm/yarn)
  5. Database (PostgreSQL/Neo4j/MongoDB/SQLite/None/Multiple)
  6. Testing framework (Vitest/Jest/Playwright/None)
  7. Dev command (e.g., "npm run dev", "bun dev")
  8. Test command (e.g., "npm test", "vitest", "None")
  9. Build command (e.g., "npm run build", "bun run build")
</gather-info>
<update-files>
  Replace placeholders in:
  - .claude/CLAUDE.md: {{PROJECT_NAME}}, {{PROJECT_DESCRIPTION}}, {{TECH_STACK}}, {{PACKAGE_MANAGER}}, {{TEST_FRAMEWORK}}, {{DATABASE_INFO}}, {{KEY_DEV_COMMAND}}, {{KEY_TEST_COMMAND}}, {{KEY_BUILD_COMMAND}}
  - docs/README.md: {{PROJECT_NAME}}
  - docs/roadmaps/mvp.md: {{PROJECT_NAME}}
  - .claude/.mcp.json: Add filesystem server; add context7 if - trigger: svelte, sveltekit, next, nextjs, react
</update-files>
<create-adr>
  Using Adr.md as the index template, create docs/adrs/README.md.
  Using adr-entry.md as the entry template, create docs/adrs/001-initial-tech-stack.md documenting the stack choice with rationale.
</create-adr>
<summary>
  Show: project name, stack, location, next steps (install, dev, review roadmap), active hooks.
</summary>
<error-handling>
  - Warn if placeholders remain after updates
</error-handling>