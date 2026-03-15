# Project Overview - Career & Skills Hub

## Goal
Career & Skills Hub is a unified web platform that combines career discovery, personal productivity, and professional knowledge sharing in a single bilingual ecosystem.

---

## Platform Modules

### 1. Job Board
- Browse and search real job listings via Adzuna API
- Filter jobs by category and keyword
- Save favorite jobs to personal dashboard
- AI-powered job recommendations based on user skills

### 2. Task & Project Management
- Create and manage personal tasks
- Kanban-style board with three statuses: To Do / In Progress / Done
- Set deadlines and priorities
- Track productivity from the dashboard

### 3. Knowledge Exchange
- Experts publish articles, tutorials, and professional tips
- Users browse and read expert content
- Articles organized by category: Tips / Tutorial / Advice
- Full Arabic translation support

---

## Key Features
- ✅ Bilingual interface: English & Arabic with automatic RTL layout
- ✅ Role-based access: User / Expert / Admin
- ✅ JWT Authentication
- ✅ Real-time job search via Adzuna API
- ✅ Responsive design for mobile and desktop
- ✅ Expert-only article publishing
- ✅ Personalized dashboard

---

## Tech Stack

| Layer | Technology |
|-------|-----------|
| Frontend | React + Vite + Tailwind CSS |
| Backend | Node.js + Express + TypeScript |
| ORM | Prisma v5 |
| Database | PostgreSQL |
| Auth | JWT |
| Job API | Adzuna API |
| i18n | i18next |

---

## How to Run

### Prerequisites
- Node.js v18+
- PostgreSQL installed and running

### Setup
```bash
# 1. Clone the repo
git clone https://github.com/your-repo/career-skills-hub

# 2. Install backend dependencies
cd backend
npm install

# 3. Set up environment variables
# Edit backend/.env and add your DATABASE_URL

# 4. Push database schema
npx prisma db push

# 5. Start backend (port 5000)
npm run dev

# 6. Install frontend dependencies
cd ../frontend
npm install

# 7. Start frontend (port 5173)
npm run dev
```

### Access
Open your browser at: `http://localhost:5173`
