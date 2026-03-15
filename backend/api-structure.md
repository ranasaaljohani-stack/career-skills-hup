# Backend - Career & Skills Hub

## Tech Stack
- **Runtime:** Node.js
- **Framework:** Express.js + TypeScript
- **ORM:** Prisma v5
- **Database:** PostgreSQL
- **Auth:** JWT (JSON Web Tokens)
- **Port:** 5000

---

## Authentication API

| Method | Endpoint | Description | Access |
|--------|----------|-------------|--------|
| POST | `/api/auth/register` | Register new user | Public |
| POST | `/api/auth/login` | Login and get JWT token | Public |

---

## Jobs API

| Method | Endpoint | Description | Access |
|--------|----------|-------------|--------|
| GET | `/api/jobs/search` | Search real jobs via Adzuna API | User |
| GET | `/api/jobs/favorites` | Get user's saved jobs | User |
| POST | `/api/jobs/favorites` | Save a job to favorites | User |
| DELETE | `/api/jobs/favorites/:id` | Remove a saved job | User |
| POST | `/api/jobs` | Add a job posting | Admin |
| PUT | `/api/jobs/:id` | Edit a job posting | Admin |
| DELETE | `/api/jobs/:id` | Remove a job posting | Admin |

---

## Tasks API

| Method | Endpoint | Description | Access |
|--------|----------|-------------|--------|
| GET | `/api/tasks` | Get all user tasks | User |
| POST | `/api/tasks` | Create a new task | User |
| PUT | `/api/tasks/:id` | Update task status/details | User |
| DELETE | `/api/tasks/:id` | Delete a task | User |

---

## Articles API

| Method | Endpoint | Description | Access |
|--------|----------|-------------|--------|
| GET | `/api/articles` | Get all published articles | Public |
| GET | `/api/articles/:id` | Get single article | Public |
| POST | `/api/articles` | Create a new article | Expert |
| PUT | `/api/articles/:id` | Edit an article | Expert/Admin |
| DELETE | `/api/articles/:id` | Remove an article | Admin |

---

## Recommendations API

| Method | Endpoint | Description | Access |
|--------|----------|-------------|--------|
| GET | `/api/recommendations/jobs` | AI-suggested jobs based on user skills | User |
| GET | `/api/recommendations/articles` | AI-suggested articles based on interests | User |

---

## Role-Based Access Control
- **USER** — Browse jobs, manage tasks, read articles
- **EXPERT** — All USER permissions + publish articles
- **ADMIN** — All permissions + manage all content and users
