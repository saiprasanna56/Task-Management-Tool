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
