# 🧠 Task Management Tool

A full-stack Kanban-style Task Management Tool built with:

- **Frontend**: React.js
- **Backend**: Node.js + Express.js
- **Database**: PostgreSQL
- **Authentication**: JWT-based Auth with Role-Based Access (Admin/Member)
- **Containerization**: Docker & Docker Compose

  Deployment link - [https://task-manager-version1-eight.vercel.app/](https://task-manager-v3-uetl.vercel.app/)

---

## 🔧 Features

- ✅ User Authentication (Login/Register)
- 🛡️ Role-Based Access Control (Admin & Member)
- 📌 Task Management (Add/Edit/Delete/Assign/Change Status)
- 🗂️ Kanban Board View
- 👥 Team & Member Management
- 📊 Dashboard with Task Overview
- 🌐 RESTful API with error handling
- 📦 Dockerized for easy deployment

---

## 🚀 Getting Started
---

## 🖥️ Local Setup (without Docker)

### 1. Clone the Repository

```bash
git clone https://github.com/your-username/task-management-tool.git
cd task-management-tool
```
### Setup Backend
```bash
cd server
npm install
```
# Create .env with DB connection, JWT_SECRET etc.
```bash
npm start
```
### Setup Frontend
```
cd client
npm install
npm start
```
## 🐳 Docker Setup (Recommended)
### 1. Prerequisites
Docker

Docker Compose

## Run with Docker Compose
```bash
docker-compose up --build
```
The app will be available at:

Frontend: http://localhost:3000

Backend: http://localhost:5000

## 🧪 API Endpoints (Sample)
## 🔐 Auth
```bash
POST /api/auth/register
POST /api/auth/login
```
## 📋 Tasks
```bash
GET    /api/tasks/tasks
POST   /api/tasks/tasks
PATCH  /api/tasks/:id
DELETE /api/tasks/:id
```
## 👥 Admin
```bash
GET    /api/admin/user
POST   /api/admin/members
DELETE /api/admin/members/:id
```
