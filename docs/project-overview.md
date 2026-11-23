# StartupHub – Project Overview

## 1. Introduction

StartupHub is a web-based incubation management platform designed to support the interaction between student founders, startup teams, administrators, and mentors. The platform aims to manage the startup incubation process from registration and application submission through screening, evaluation, approval, mentorship, and progress monitoring.

## 2. Problem Statement

Startup incubation activities can involve multiple people, documents, reviews, and stages. When these activities are managed through disconnected tools or manual processes, it can become difficult to track application status, coordinate evaluations, maintain records, and monitor startup progress.

StartupHub aims to bring these activities into one organized platform.

## 3. Objectives

- Provide a central platform for startup registration and applications.
- Allow students to submit information and track application progress.
- Help administrators review, screen, and manage applications.
- Allow mentors to guide assigned startups and record progress.
- Maintain structured records of applications, evaluations, and mentorship.
- Provide administrators with an overview of incubation activities.

## 4. User Roles

### Student / Startup Founder

- Register and sign in.
- Complete a personal profile.
- Create and maintain startup information.
- Add startup team members.
- Submit applications and required documents.
- Track application status and review feedback.
- View mentorship details and progress information when applicable.

### Administrator

- Access the administration dashboard.
- Manage user and startup records.
- Review submitted applications and documents.
- Conduct screening and request corrections.
- Coordinate evaluations and record decisions.
- Assign mentors to approved startups.
- Monitor incubation progress and view reports.

### Mentor

- Access assigned startup information.
- Review startup profiles and relevant documents.
- Provide guidance and evaluation feedback.
- Schedule or record mentorship sessions.
- Review milestones and update progress notes.

## 5. Main Functional Modules

1. Authentication and role management
2. Student profile management
3. Startup and team management
4. Application submission and tracking
5. Screening and document review
6. Evaluation and decision management
7. Mentor assignment and mentorship sessions
8. Milestones and progress reports
9. Notifications and announcements
10. Administrative dashboard and reports

## 6. Proposed Application Lifecycle

The following lifecycle is a starting proposal and must be confirmed with the incubation organization:

```text
Draft
  |
  v
Submitted
  |
  v
Under Screening
  |
  +----> Correction Required ----> Resubmitted
  |                                  |
  +----------------------------------+
  |
  v
Under Evaluation
  |
  v
Shortlisted
  |
  +----> Approved ----> Incubating
  |
  +----> Rejected
```

The final statuses, decision rules, and who can change each status should be confirmed before implementation.

## 7. Technology Stack

| Layer | Technology |
|---|---|
| Frontend | React, JavaScript, Vite |
| Backend | Node.js, Express.js |
| Database | Supabase (PostgreSQL) |

The planned backend will connect to Supabase PostgreSQL using `pg` and SQL queries. Prisma is not included.

## 8. Project Scope

The initial scope covers the three user roles and the core startup application and incubation workflows. Features such as automated document verification, advanced analytics, and external integrations may be considered later.

## 9. Current Status

The project currently has a Figma-generated frontend source. Backend services, database schema, authentication, and full integration are planned and should not be considered implemented until completed and tested.
