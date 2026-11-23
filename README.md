# StartupHub – Incubation Management Platform

StartupHub is a web-based incubation management platform intended to connect students and startup founders, administrators, and mentors. It aims to organize startup registration, application submission, screening, evaluation, mentorship, and progress tracking in one place.

> **Project status:** Under development. The current repository begins with frontend. Backend APIs and Supabase database integration are planned implementation work.

## Planned Features

- Separate dashboards for Students, Administrators, and Mentors
- Student profile and startup management
- Startup registration and application submission
- Document submission and application tracking
- Application screening, evaluation, and approval
- Mentor assignment and mentorship sessions
- Startup milestones and progress reports
- Administrative reporting and notifications

## Technology Stack

| Layer | Technology |
|---|---|
| Frontend | React, JavaScript, Vite |
| Backend | Node.js, Express.js |
| Database | Supabase (PostgreSQL) |

The backend is planned to connect to Supabase PostgreSQL using the `pg` package and SQL queries. Prisma is not part of the planned stack.

## User Roles

| Role | Main responsibilities |
|---|---|
| Student / Startup Founder | Maintain a profile, register a startup, submit applications, upload documents, and track application progress |
| Administrator | Manage users and applications, verify submissions, conduct screening, coordinate evaluations, and monitor incubated startups |
| Mentor | View assigned startups, provide guidance, record evaluations, and monitor milestones |

## High-Level Architecture

```text
Student / Administrator / Mentor
               |
               v
       React Frontend
        JavaScript + Vite
               |
          REST API / JSON
               |
               v
       Node.js + Express
     Authentication, Access
       Control, Business Logic
               |
          SQL Queries
               |
               v
      Supabase PostgreSQL
```

See [System Architecture](docs/system-architecture.md) for more detail.

## Planned Repository Structure

```text
startuphub-incubation-platform/
├── frontend/                 # React frontend
├── backend/                  # Node.js and Express API
├── supabase/
│   ├── migrations/           # SQL database migrations
│   └── seed.sql              # Optional development seed data
├── docs/                     # Project documentation
├── .env.example
├── .gitignore
└── README.md
```

The actual structure may evolve during implementation. The existing Figma-exported frontend should be preserved while it is reorganized.

## Getting Started

Setup instructions will be added after the frontend and backend folders are finalized.

### Planned local development

1. Install a supported Node.js LTS version.
2. Install frontend dependencies inside `frontend/`.
3. Install backend dependencies inside `backend/`.
4. Create a Supabase project and configure the backend environment variables.
5. Apply the SQL migrations in `supabase/migrations/`.
6. Start the frontend and backend development servers.

Do not commit real `.env` files, database passwords, JWT secrets, or Supabase service-role keys.

## Documentation

- [Project Overview](docs/project-overview.md)
- [System Architecture](docs/system-architecture.md)
- [Database Design](docs/database-design.md)
- [API Documentation](docs/api-documentation.md)
- [Contributing Guidelines](CONTRIBUTING.md)
- [Changelog](CHANGELOG.md)


## Contributors

Add project contributors and their responsibilities here.

## License

A license has not yet been selected. Until one is added, do not assume that this repository grants permission to reuse, distribute, or modify the code.
