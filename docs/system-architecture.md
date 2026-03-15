# System Architecture - Career & Skills Hub

## Architecture Overview
Single-repository full-stack web application with a React frontend and a unified Node.js/Express backend connected to a PostgreSQL database.

---

## Folder Structure

```
career-skills-hub/
├── frontend/                  # React + Vite + Tailwind
│   ├── src/
│   │   ├── components/        # Reusable UI components
│   │   ├── pages/             # Page-level components
│   │   ├── context/           # Auth context (JWT)
│   │   ├── api/               # API call functions
│   │   └── locales/           # en.json & ar.json translations
│   └── package.json
│
├── backend/                   # Node.js + Express + TypeScript
│   ├── src/
│   │   ├── controllers/       # Route logic
│   │   ├── routes/            # API route definitions
│   │   ├── middlewares/       # Auth & role middleware
│   │   └── utils/             # Helper functions
│   ├── prisma/
│   │   └── schema.prisma      # Database schema
│   └── package.json
│
├── database/
│   └── schema.md              # Database documentation
│
├── docs/
│   ├── project-overview.md
│   ├── system-architecture.md
│   └── project-prompt.md
│
└── README.md
```

---

## Data Flow

```
User (Browser)
     ↓
React Frontend (port 5173)
     ↓ HTTP requests
Express Backend (port 5000)
     ↓ Prisma ORM
PostgreSQL Database
     
Backend also calls:
     → Adzuna API (real job listings)
```

---

## Authentication Flow

```
1. User submits login form
2. Backend validates credentials
3. Backend returns JWT token
4. Frontend stores token in context
5. All protected API calls include token in header
6. Backend middleware validates token on each request
```

---

## Role Permissions

| Feature | USER | EXPERT | ADMIN |
|---------|------|--------|-------|
| Browse jobs | ✅ | ✅ | ✅ |
| Save jobs | ✅ | ✅ | ✅ |
| Manage tasks | ✅ | ✅ | ✅ |
| Read articles | ✅ | ✅ | ✅ |
| Publish articles | ❌ | ✅ | ✅ |
| Manage all content | ❌ | ❌ | ✅ |
| Manage users | ❌ | ❌ | ✅ |
