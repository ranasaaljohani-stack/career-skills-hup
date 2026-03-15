# Database Schema - Career & Skills Hub

## Database: PostgreSQL
## ORM: Prisma v5

---

## Users Table

| Column | Type | Description |
|--------|------|-------------|
| id | String (UUID) | Primary key |
| name | String | Full name |
| email | String | Unique email |
| password | String | Hashed password |
| role | Enum | USER / EXPERT / ADMIN |
| skills | String[] | List of user skills |
| createdAt | DateTime | Account creation date |

---

## Jobs Table

| Column | Type | Description |
|--------|------|-------------|
| id | String (UUID) | Primary key |
| title | String | Job title |
| company | String | Company name |
| location | String | Job location |
| salary | String | Salary range |
| description | String | Full job description |
| category | String | Job category |
| tags | String[] | Related skills/tags |
| createdAt | DateTime | Date posted |

---

## Tasks Table

| Column | Type | Description |
|--------|------|-------------|
| id | String (UUID) | Primary key |
| userId | String | Owner (foreign key → Users) |
| title | String | Task title |
| status | Enum | TODO / IN_PROGRESS / DONE |
| deadline | DateTime | Due date |
| priority | Enum | LOW / MEDIUM / HIGH |
| createdAt | DateTime | Creation date |

---

## Articles Table

| Column | Type | Description |
|--------|------|-------------|
| id | String (UUID) | Primary key |
| authorId | String | Expert (foreign key → Users) |
| title | String | Article title |
| content | String | Full article content |
| category | Enum | TIPS / TUTORIAL / ADVICE |
| tags | String[] | Related topics |
| approved | Boolean | Approved by admin |
| createdAt | DateTime | Publish date |

---

## Favorites Table

| Column | Type | Description |
|--------|------|-------------|
| id | String (UUID) | Primary key |
| userId | String | User (foreign key → Users) |
| jobId | String | Saved job ID |
| jobTitle | String | Job title (cached) |
| company | String | Company name (cached) |
| createdAt | DateTime | Date saved |
