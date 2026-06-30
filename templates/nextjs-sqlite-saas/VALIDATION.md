# Validation Notes

Issue: [#2](https://github.com/claude-builders-bounty/claude-builders-bounty/issues/2)

## Greenfield Project Check

The template was checked against a standard greenfield project shape:

```bash
npx create-next-app@latest acme-saas --ts --app --tailwind --eslint
cd acme-saas
npm install better-sqlite3 zod
mkdir -p app/'(app)'/dashboard components/ui db/migrations db/queries lib/validation tests/integration
cp ../CLAUDE.md ./CLAUDE.md
```

## Expected Claude Code Behavior

After reading the template, Claude Code has enough context to proceed without
asking clarifying questions for these common tasks:

1. Add a workspace table and numbered SQLite migration.
2. Create a Server Action for a validated workspace form.
3. Add a dashboard page that reads data through `db/queries`.
4. Explain why SQL should stay out of Client Components.

## Coverage Against Acceptance Criteria

- Stack and versions: covered in `Stack And Versions`.
- Folder structure: covered in `Project Shape`.
- Naming conventions: covered in `Naming Conventions`.
- Database migration rules: covered in `SQLite And Migration Rules`.
- Dev commands: covered in `Commands`.
- Patterns to follow: covered in App Router, Server Actions, Components, Auth,
  Database Access, and Testing sections.
- Anti-patterns with reasons: covered in `Anti-Patterns To Avoid`.
- Usable without modification: the file intentionally uses project-relative
  folders and commands for a greenfield Next.js 15 + SQLite SaaS app.
