# Jira Clone — Kanban Project Management Tool

A full-stack Kanban board application inspired by Atlassian Jira, built with the MERN Stack as part of the MERN Stack Developer Intern Technical Assessment.

🔗 **Live Demo:** https://jira-clone-xi.vercel.app  
🔗 **Backend API:** https://jira-clone-cmq7.onrender.com  
🔗 **GitHub:** https://github.com/Prem-0007/jira-clone

---

## Features

- 🔐 JWT Authentication (Signup / Login / Logout)
- 📋 Three-column Kanban Board (To Do / In Progress / Done)
- 🎯 Priority Levels (Low / Medium / High)
- 🖱️ Drag and Drop tasks between columns
- ➕ Create / Edit / Delete issues
- ◀▶ Move tasks between columns with buttons
- 👤 User-specific tasks (each user sees only their own)
- ✅ Input validation on both frontend and backend
- 📱 Responsive Design (mobile friendly)

---

## Tech Stack

| Layer | Technology |
|-------|-----------|
| Frontend | React, React Router, Axios, Vite |
| Backend | Node.js, Express.js |
| Database | MongoDB Atlas, Mongoose |
| Auth | JWT, Bcrypt |
| Deployment | Vercel (frontend), Render (backend) |

---

## Project Structure

```
jira-clone/
├── backend_task3/
│   ├── src/
│   │   ├── middlewares/
│   │   │   └── authMiddleware.mjs
│   │   ├── mongoose/
│   │   │   └── schemas/
│   │   │       ├── task.mjs
│   │   │       └── user.mjs
│   │   ├── routes/
│   │   │   ├── authRoutes.mjs
│   │   │   └── routes.mjs
│   │   └── utils/
│   │       ├── password.mjs
│   │       ├── validationSchema.mjs
│   │       └── resolveIndexID.mjs
│   ├── .env
│   ├── package.json
│   └── index.mjs
│
└── frontend_task3/
    ├── src/
    │   ├── pages/
    │   │   ├── Dashboard.jsx
    │   │   ├── Login.jsx
    │   │   └── Signup.jsx
    │   ├── App.jsx
    │   ├── App.css
    │   └── api.js
    ├── .env
    ├── index.html
    └── package.json
```

---

## Local Setup Instructions

### 1. Clone the repo
```bash
git clone https://github.com/Prem-0007/jira-clone.git
cd jira-clone
```

### 2. Backend Setup
```bash
cd backend_task3
npm install
```

Create `.env` file inside `backend_task3/`:
```
PORT=3000
MONGO_URI=your_mongodb_atlas_connection_string
JWT_SECRET=your_jwt_secret_key
```

```bash
node index.mjs
# Server runs on http://localhost:3000
```

### 3. Frontend Setup
```bash
cd frontend_task3
npm install
```

Create `.env` file inside `frontend_task3/`:
```
VITE_API_URL=http://localhost:3000
```

```bash
npm run dev
# App runs on http://localhost:5173
```

---

## API Endpoints

### Auth Routes — `/api/auth`

| Method | Endpoint | Description |
|--------|----------|-------------|
| POST | /api/auth/signup | Register new user |
| POST | /api/auth/login | Login user, returns JWT |
| POST | /api/auth/logout | Logout user |
| GET | /api/auth/status | Check auth status |

### Task Routes — `/api/tasks`

| Method | Endpoint | Description |
|--------|----------|-------------|
| GET | /api/tasks | Get all tasks for logged in user |
| GET | /api/tasks/:id | Get single task |
| POST | /api/tasks | Create new task |
| PUT | /api/tasks/:id | Update task (title, status, priority) |
| PATCH | /api/tasks/:id | Partial update task |
| DELETE | /api/tasks/:id | Delete task |

---

## Environment Variables

### Backend
| Variable | Description |
|----------|-------------|
| PORT | Server port (default: 3000) |
| MONGO_URI | MongoDB Atlas connection string |
| JWT_SECRET | Secret key for JWT signing |

### Frontend
| Variable | Description |
|----------|-------------|
| VITE_API_URL | Backend API base URL |

---

## Deployment

- **Frontend** deployed on [Vercel](https://vercel.com)
- **Backend** deployed on [Render](https://render.com)
- **Database** hosted on [MongoDB Atlas](https://www.mongodb.com/atlas)

---

Built with ❤️ by [Prem Kumar Balla](https://github.com/Prem-0007)
