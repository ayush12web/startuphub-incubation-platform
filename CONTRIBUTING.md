# Contributing to StartupHub

Thank you for contributing to the StartupHub Incubation Management Platform.

This document describes the basic workflow expected for project contributions. Update these guidelines as the team and development process grow.

## Before You Start

1. Read the project [README](README.md).
2. Review the relevant documents in the `docs/` directory.
3. Check existing issues or discuss the proposed change with the project team.
4. Do not commit secrets, credentials, private user information, or production data.

## Development Principles

- Preserve the existing Figma-generated design unless a design change is agreed upon.
- Use JavaScript (`.js` and `.jsx`) for the frontend.
- Use Node.js and Express.js for the backend.
- Use Supabase PostgreSQL as the database.
- Use SQL queries through the backend `pg` connection; Prisma is not part of the project stack.
- Keep frontend and backend responsibilities separate.
- Validate incoming data on the backend.
- Enforce permissions on the backend, not only by hiding frontend controls.
- Write clear, descriptive names and keep functions focused.

## Branching

Use descriptive branch names:

```text
feature/student-registration
feature/admin-screening
fix/login-validation
docs/update-database-design
```

Avoid committing directly to the main branch when working in a team. Use a pull request so changes can be reviewed.

## Commit Messages

Use concise messages that explain the change:

```text
feat: add student registration page
fix: validate startup application fields
docs: update system architecture
refactor: organize frontend components
```

## Pull Request Checklist

Before opening a pull request:

- [ ] The change has a clear description.
- [ ] Related documentation has been updated.
- [ ] No `.env` files, passwords, tokens, or private keys are included.
- [ ] The application builds or runs as expected.
- [ ] Relevant manual or automated tests have been completed.
- [ ] The pull request does not include unrelated changes.

## Reporting Bugs

When reporting a bug, include:

- A clear summary
- Steps to reproduce
- Expected behavior
- Actual behavior
- Relevant error messages or screenshots (remove secrets and personal data)

## Questions and Suggestions

Discuss major architecture, database, or workflow changes with the project team before implementing them.
