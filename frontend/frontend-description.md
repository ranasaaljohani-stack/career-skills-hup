# Frontend - Career & Skills Hub

## Tech Stack
- **Framework:** React (Vite)
- **Styling:** Tailwind CSS
- **Icons:** Lucide React
- **Language Support:** i18next (English & Arabic with RTL)
- **Auth:** JWT stored in context

---

## Pages & Components

### 1. Login Page (`/login`)
- Email and password fields
- JWT token stored on success
- Redirects to Dashboard

### 2. Register Page (`/register`)
- Name, email, password fields
- Role selection: User / Expert
- Redirects to Login on success

### 3. Dashboard (`/dashboard`)
- Summary statistics (tasks, saved jobs, articles)
- Quick view of saved jobs
- Quick view of active tasks
- Expert articles feed

### 4. Job Board (`/jobs`)
- Real-time job search via Adzuna API
- Keyword search bar
- Category filter
- Job cards showing: title, company, location, salary
- Save/Favorite button per job

### 5. Task Manager (`/tasks`)
- Kanban-style board
- Three columns: To Do / In Progress / Done
- Create new task with title, deadline, priority
- Drag or update task status

### 6. Knowledge Hub (`/knowledge`)
- Article feed from verified experts
- Article cards: title, author, category, preview, date
- Read More modal with full article content
- Write Article button (visible to EXPERT role only)
- Article creation form: title, category, content, tags

---

## Bilingual Support
- Language toggle button (EN / AR) in the navbar
- Full RTL layout when Arabic is selected
- All UI strings stored in:
  - `src/locales/en.json`
  - `src/locales/ar.json`
