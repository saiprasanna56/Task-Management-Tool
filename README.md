# 🎯 Task Manager – React App

Welcome to the **Task Manager** — a modern, full-featured task management web application built with **React**, backed by **Node.js**, **PostgreSQL**, and powered with **Docker** for seamless deployment.

> Built with 💙 using Create React App

---

## 🚀 Features

- ✅ Create, edit, and delete tasks
- 🗂️ Set due dates, priorities, and assign users
- 📬 User authentication with secure registration & login
- 📊 Filter tasks by status and priority
- 🌐 Full Docker integration
- 🧩 PostgreSQL as a powerful relational database

## DEPLOYMENT FRONTEND LINK - [Deployment link](https://task-management-tool-two.vercel.app/)

---

## 🛠️ Available Scripts

In the project directory, you can run:

### ▶️ `npm start`

Runs the app in the development mode.  
Open [http://localhost:3000](http://localhost:3000) to view it in your browser.  
Hot-reloading is enabled.

---

### 🧪 `npm test`

Launches the test runner in the interactive watch mode.  
More info: [Running Tests](https://facebook.github.io/create-react-app/docs/running-tests)

---

### 🏗️ `npm run build`

Builds the app for production to the `build/` folder.  
The build is minified and the filenames include hashes.

📘 Learn about: [Deployment](https://facebook.github.io/create-react-app/docs/deployment)

---

### 🛑 `npm run eject` (Advanced)

> **Warning**: This is a one-way operation!

Exposes all configuration files and dependencies like Webpack, Babel, ESLint, etc.

---

## 🐳 Dockerized Deployment

### 🔨 Build Docker Image
```bash
docker build -t veeru0115/client .



git init
git add README.md
git commit -m "first commit"
git branch -M main
git remote add origin git@github.com:veerendra17788/taskManager.git
git push -u origin main
=======
# taskManager
=======
# 🗂️ Task Management Tool

A full-stack task management application built with React, Node.js, Express, and PostgreSQL. It supports user registration/login, role-based access (Admin & Member), and Kanban-style task management.
Setuphe Repository

```bash
git clone https://github.com/your-username/task-management-tool.git
cd task-management-tool
```
### 2.Setup backend
```bash
Copy
Edit
cd server
npm install
```

### Create a .env file inside server/:

```env
PORT=5000
DATABASE_URL=postgresql://your_username:your_password@localhost:5432/your_db_name
JWT_SECRET=your_secret_key
```

### Initialize the database (PostgreSQL):

```sql
CREATE DATABASE your_db_name;
```
-- Use schema.sql or run the migrations manually

### Start the backend:

```bash
npm run dev
Setup frontend
```
```bash
cd ../client
npm install
npm start
```
Frontend runs at http://localhost:3000, backend at http://localhost:5000.

## 🐳 Docker Setup (Optional)
Make sure Docker is installed.

### 1. Build and run using Docker Compose:
```bash
docker-compose up --build
```

This sets up:

- Node.js backend (server)

- PostgreSQL database

- React frontend (client)

### 2. Environment Variables
Edit the .env file (already configured in docker-compose.yml).

No need to install dependencies manually.

### 3. Access the App
- React frontend: http://localhost:3000

- API server: http://localhost:5000

- PostgreSQL (port 5432 inside Docker)

### 📬 API Documentation (Postman)

| Method | Endpoint              | Description           |
|--------|------------------------|-----------------------|
| POST   | `/api/auth/login`      | Login user            |
| POST   | `/api/auth/register`   | Register user         |
| GET    | `/api/users`           | Get all users (admin) |
| DELETE | `/api/users/:id`       | Delete user (admin)   |
| GET    | `/api/tasks`           | Get all tasks         |
| POST   | `/api/tasks`           | Create new task       |
| PUT    | `/api/tasks/:id`       | Update task           |
| DELETE | `/api/tasks/:id`       | Delete task           |

Each request returns JSON with status codes (200, 400, 401, 404, etc.).

### 🔒 Authentication
JWT tokens are returned after login or registration.

Add to headers:

```http
Authorization: Bearer <your_token_here>
```

### 🧪 Tech Stack
- React (Frontend)

- Node.js + Express (Backend)

- PostgreSQL (Database)

- JWT (Auth)

- React Router, Axios

- react-beautiful-dnd (Kanban)

- Docker (optional)