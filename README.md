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
