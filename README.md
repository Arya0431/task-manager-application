# Task Manager System

A full-stack task management application with Role-Based Access Control (RBAC).

## 🚀 Overview

This project includes:
- Admin features for managing users and tasks
- User features for viewing assigned tasks, updating status, and adding comments
- React + TypeScript + Vite + Tailwind CSS frontend
- Node.js + Express + Sequelize backend
- MySQL database
- JWT authentication and bcryptjs password hashing

---

## ✨ Features

- Secure login with JWT
- Admin and User role separation
- Admin dashboard with stats
- Create, edit, delete users
- Create, assign, edit, delete tasks
- Task status updates
- Task comments
- CSV export for tasks
- Fully responsive UI

---

## 🛠 Tech Stack

Frontend:
- React
- TypeScript
- Vite
- Tailwind CSS
- Axios
- React Router

Backend:
- Node.js
- Express.js

Database:
- MySQL

ORM:
- Sequelize

Authentication:
- JWT
- bcryptjs

---

## 📁 Project Structure

task-manager/
├── backend/
│   ├── config/
│   ├── middleware/
│   ├── models/
│   ├── routes/
│   ├── utils/
│   ├── .env.example
│   ├── package.json
│   └── server.js
├── frontend/
│   ├── src/
│   ├── .env.example
│   └── package.json
├── render.yaml
└── start.sh

---

## 🗄 Database Tables

Users:
- id
- name
- email
- password
- role

Tasks:
- id
- title
- description
- assigned_to
- priority
- status
- due_date

Comments:
- id
- task_id
- user_id
- content

---

## ⚙️ Local Setup

1. Clone Repository

git clone https://github.com/your-username/task-manager.git
cd task-manager

---

2. Backend Setup

Create .env inside backend/

PORT=5000
CLIENT_URL=http://localhost:5173
JWT_SECRET=replace_with_a_secure_secret
DB_HOST=localhost
DB_PORT=3306
DB_NAME=task_manager
DB_USER=root
DB_PASSWORD=
DB_SYNC=true
DB_SYNC_ALTER=false

---

3. Frontend Setup

Create .env inside frontend/

VITE_API_URL=http://localhost:5000

---

4. Install Dependencies

cd backend
npm install

cd ../frontend
npm install

---

5. Run Project

Option 1:

./start.sh

Option 2:

# Backend
cd backend
npm run dev

# Frontend
cd frontend
npm run dev

---

## 🌐 Default URLs

Frontend: http://localhost:5173  
Backend: http://localhost:5000  
Health Check: http://localhost:5000/health  

---

## 🚀 Render Deployment

Steps:

1. Push project to GitHub  
2. Open Render Dashboard  
3. Click "New Blueprint Instance"  
4. Select repository  
5. Fill environment variables  

---

Backend Environment:

NODE_ENV=production
PORT=5000
CLIENT_URL=https://your-frontend.onrender.com
JWT_SECRET=your_secure_secret
DB_HOST=your_mysql_host
DB_PORT=3306
DB_NAME=your_database_name
DB_USER=your_database_user
DB_PASSWORD=your_database_password
DB_SYNC=true
DB_SYNC_ALTER=false

---

Frontend Environment:

VITE_API_URL=https://your-backend.onrender.com

---

## 📡 API Overview

Auth:
- POST /api/auth/register
- POST /api/auth/login

Users:
- GET /api/users
- POST /api/users
- PUT /api/users/:id
- DELETE /api/users/:id

Tasks:
- GET /api/tasks
- GET /api/tasks/my
- POST /api/tasks
- PUT /api/tasks/:id
- DELETE /api/tasks/:id
- PATCH /api/tasks/:id/status
- GET /api/tasks/:id/comments
- POST /api/tasks/:id/comments

---

## 🔐 RBAC Summary

Admin:
- Manage users
- Create, assign, edit, delete tasks
- View all tasks
- Export reports
- View dashboard stats

User:
- View assigned tasks
- Update task status
- Add comments

---

## 📌 Notes

- Frontend uses VITE_API_URL
- Backend uses CLIENT_URL for CORS
- Health endpoint: /health
- MySQL must be running before backend

---

## 📄 License

This project is for learning and academic purposes.