# StartupHub – API Documentation (Planned)

## 1. Overview

The backend will expose REST APIs using Node.js and Express.js. The frontend will communicate with these endpoints using HTTP requests and JSON.

**Proposed base URL (local):**

```text
http://localhost:5000/api/v1
```

The endpoints below are a planning draft. They are not implemented until corresponding backend routes and controllers are created.

## 2. Authentication

| Method | Endpoint | Purpose | Access |
|---|---|---|---|
| POST | `/auth/register` | Register a user | Public |
| POST | `/auth/login` | Sign in | Public |
| POST | `/auth/logout` | Sign out | Authenticated |
| GET | `/auth/me` | Get current user details | Authenticated |

## 3. Student and Profile APIs

| Method | Endpoint | Purpose | Access |
|---|---|---|---|
| GET | `/students/profile` | Get student profile | Student |
| PUT | `/students/profile` | Update student profile | Student |
| GET | `/students/dashboard` | Get student dashboard data | Student |

## 4. Startup APIs

| Method | Endpoint | Purpose | Access |
|---|---|---|---|
| POST | `/startups` | Create a startup | Student |
| GET | `/startups` | List startups visible to the user | Role-dependent |
| GET | `/startups/:id` | Get startup details | Authorized user |
| PUT | `/startups/:id` | Update startup details | Authorized user |
| POST | `/startups/:id/members` | Add a startup team member | Authorized user |

## 5. Application APIs

| Method | Endpoint | Purpose | Access |
|---|---|---|---|
| POST | `/applications` | Submit an application | Student |
| GET | `/applications` | List accessible applications | Role-dependent |
| GET | `/applications/:id` | Get application details | Authorized user |
| PATCH | `/applications/:id/status` | Update application status | Authorized admin |
| GET | `/applications/:id/history` | View status history | Authorized user |

## 6. Admin APIs

| Method | Endpoint | Purpose | Access |
|---|---|---|---|
| GET | `/admin/dashboard` | Get admin dashboard data | Admin |
| GET | `/admin/users` | List users | Admin |
| GET | `/admin/applications` | Review applications | Admin |
| POST | `/screenings` | Record screening result | Admin |
| POST | `/evaluations` | Record or assign evaluation | Admin |
| POST | `/mentorship/assignments` | Assign a mentor | Admin |
| GET | `/reports/dashboard` | Get report data | Admin |

## 7. Mentor APIs

| Method | Endpoint | Purpose | Access |
|---|---|---|---|
| GET | `/mentor/dashboard` | Get mentor dashboard data | Mentor |
| GET | `/mentor/startups` | List assigned startups | Mentor |
| POST | `/mentorship/sessions` | Create a mentorship session | Mentor |
| GET | `/mentorship/sessions` | View mentorship sessions | Authorized user |
| POST | `/startups/:id/progress-reports` | Submit a progress report | Assigned mentor / authorized user |

## 8. Notifications

| Method | Endpoint | Purpose | Access |
|---|---|---|---|
| GET | `/notifications` | List current user's notifications | Authenticated |
| PATCH | `/notifications/:id/read` | Mark a notification as read | Owner |

## 9. Example JSON Response

A successful API response may follow this structure:

```json
{
  "success": true,
  "message": "Application retrieved successfully",
  "data": {
    "id": "application-id",
    "status": "Under Screening"
  }
}
```

An error response may follow this structure:

```json
{
  "success": false,
  "message": "You are not authorized to access this resource"
}
```

Do not expose internal stack traces, database credentials, or sensitive information in API responses.

## 10. API Conventions

- Use appropriate HTTP methods and status codes.
- Validate request bodies, route parameters, and query parameters.
- Authenticate protected requests.
- Enforce role and record-level authorization in the backend.
- Use pagination for large lists.
- Keep response formats consistent.
- Document required fields and possible error responses as endpoints are implemented.

## 11. Implementation Status

All endpoints in this document are proposed. Update this file when routes are implemented, tested, or changed.
