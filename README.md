# 📌 Task Management App (MERN Stack)

A full-featured task management application built using the MERN stack (MongoDB, Express.js, React, Node.js). This app allows users to create, view, update, and delete tasks, complete with real-time status management and validations.

---

## 🚀 Features

- ✅ Add new tasks with title and description
- ✅ List all tasks with real-time status badges
- ✅ View detailed task info by ID
- ✅ Edit and update existing tasks
- ✅ Delete tasks with instant UI refresh
- ✅ Status badge color coding (`Pending`, `Running`, `Completed`, `Failed`)
- ✅ Robust client-side form validation using **Zod**
- ✅ Toast notifications for success and error states
- ✅ Clean React routing using **React Router**
- ✅ Connected to MongoDB Atlas via Mongoose ORM
- ✅ MVC structured backend API with RESTful endpoints

---

## 🛠️ Tech Stack

### Frontend:
- React.js (Vite)
- React Router
- Tailwind CSS
- Zod (form validation)
- Custom Toast notification utility

### Backend:
- Node.js
- Express.js
- MongoDB Atlas (via Mongoose)
- CORS, dotenv, nodemon

---

## 📁 Project Structure
📦 Task-Management-App
├── 📂 client                         # React Frontend
│   ├── 📂 components                 # Reusable components (Task, Badge, etc.)
│   │   ├── Badge.jsx
│   │   └── Task.jsx
│   │
│   ├── 📂 pages                      # React page-level components
│   │   ├── HomePage.jsx
│   │   ├── ShowTask.jsx
│   │   └── TaskListPage.jsx
│   │
│   ├── 📂 helper                     # Utility/helper functions
│   │   ├── getZodError.js
│   │   └── showToast.js
│   │
│   ├── App.jsx                       # Main App component with routes
│   ├── main.jsx                      # React app entry point
│   ├── index.css                     # Tailwind or global styles
│   ├── vite.config.js                # Vite config
│   ├── package.json
│   └── .env                          # Frontend environment config
│
├── 📂 api (or server)                # Express Backend
│   ├── 📂 controllers                # All route handlers / logic
│   │   └── taskController.js
│   │
│   ├── 📂 routes                     # API routes
│   │   └── taskRoutes.js
│   │
│   ├── 📂 models                     # Mongoose models
│   │   └── taskModel.js
│   │
│   ├── .env                          # Backend environment variables
│   ├── index.js                      # Express server entry point
│   ├── package.json
│   └── package-lock.json
│
├── .gitignore
├── README.md                         # Project overview and setup
└── 📸 (optional screenshots folder)




---

## 📦 Installation & Setup

### Backend Setup:
```bash
cd server
npm install
npm run start


PORT=4001
MONGODB_CONN=<Your MongoDB connection string>

cd client
npm install
npm run dev

| Method | Route                          | Description           |
|:--------|:--------------------------------|:----------------------|
| GET    | `/api/task/get-all-task`        | Get all tasks          |
| GET    | `/api/task/show-task/:id`       | Get a task by ID       |
| POST   | `/api/task/create-task`         | Create a new task      |
| PUT    | `/api/task/update-task/:id`     | Update an existing task|
| DELETE | `/api/task/delete-task/:id`     | Delete a task          |
