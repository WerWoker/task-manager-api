# 🧩 Task Manager API

A simple REST API built with **Flask** and **MySQL**, allowing users to manage tasks (create, view, update, delete).

## 🚀 Technologies
- Python 3
- Flask
- MySQL
- Postman (for testing)

## ⚙️ Setup

1. Clone the repository:
   ```bash
   git clone https://github.com/WerWoker/task-manager-api.git
   cd task-manager-api
2. Install dependencies:
   '''bash
   pip install -r requirements.txt
3. Create MySQL database:
   '''bash
   CREATE DATABASE task_manager;
   USE task_manager;
   CREATE TABLE tasks (
       id INT AUTO_INCREMENT PRIMARY KEY,
       title VARCHAR(255) NOT NULL,
       description TEXT,
       status ENUM('pending', 'completed') DEFAULT 'pending',
       created_at TIMESTAMP DEFAULT CURRENT_TIMESTAMP
   );
4. Run the app:
   '''bash
   python app.py

## 🧪 Testing with Postman
- GET /tasks — Get all tasks
- POST /tasks — Create new task
- PUT /tasks/<id> — Update task
- DELETE /tasks/<id> — Delete task

Example POST body:
   '''bash
   {
     "title": "Learn Flask",
     "description": "Build a REST API"
   }
