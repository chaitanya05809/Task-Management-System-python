# Task Management System

## Project created by:
Chaitanya Popat Kshirsagar  
Student of Amrutvahini College of Engineering, Electronics & Computer Engineering Department  
(under Zensar Python and SQL Training)

## Project Description
This project implements a simple task management system using Python and Flask with an SQLite database. The system includes the following components:

1. **Users:** Users can register and log in to the system.
2. **Tasks:** Users can create, view, edit, and delete tasks. Tasks have attributes such as title, description, status, due date, and the user who created the task.

## Key Features:
1. **User Authentication:** Secure user registration and login functionality.
2. **Task Management:** Create, view, update, and delete tasks.
3. **Data Persistence:** Use SQLite to store task data.
4. **REST API:** JSON-based RESTful API for interacting with the system.

## Technologies Used
- Python
- Flask
- Flask-SQLAlchemy
- SQLite
- Postman (for API testing)

## Project Structure
task_management/ |-- app.py|-- models.py|-- config.py|-- requirements.txt


## Setup
1. **Clone the repository:**
   ```bash
   git clone https://github.com/yourusername/task_management.git
   cd task_management
2. **Create a virtual environment and activate it:**
   python -m venv venv
   source venv/bin/activate   # On Windows use `venv\Scripts\activate`
   
4. **Install the required packages:**
   pip install -r requirements.txt

5. **Run the Flask application:**
   python app.py

# API Endpoints

## User Authentication

Register: 

1)  Endpoint: /register  
2)  Method: POST  
3)  Description: Register a new user  
4)  Request Body: { "username": "your_username", "password": "your_password" }

Login:  

1)  Endpoint: /login  
2)  Method: POST  
3)  Description: Authenticate user and get JWT token  
4)  Request Body: { "username": "your_username", "password": "your_password" }

## Task Management

Get All Tasks:  

1)  Endpoint: /tasks  
2)  Method: GET  
3)  Description: Retrieve all tasks for the authenticated user  
4)  Headers: Authorization: Bearer <JWT_TOKEN>


Create Task:  

1)  Endpoint: /tasks  
2)  Method: POST  
3)  Description: Create a new task  
4)  Headers: Content-Type: application/json, Authorization: Bearer <JWT_TOKEN>  
5)  Request Body:

```json
{
  "title": "Buy groceries",
  "description": "Milk, Eggs, Bread",
  "status": "Pending",
  "due_date": "2025-01-10"
}
````
Update Task:  

1)  Endpoint: /tasks/<task_id>  
2)  Method: PUT  
3)  Description: Update an existing task  
4)  Headers: Content-Type: application/json, Authorization: Bearer <JWT_TOKEN>  
5)  Request Body:
   
```json 
{
  "title": "Buy vegetables",    
  "description": "Tomatoes, Spinach",  
  "status": "Completed",  
  "due_date": "2025-01-09"  
}
````
        
Delete Task:  

1)  Endpoint: /tasks/<task_id>  
2)  Method: DELETE  
3)  Description: Delete a task  
4)  Headers: Authorization: Bearer <JWT_TOKEN>  


## Guidance:
Project created under the guidance of Sir Aniruddh Gaikwad.
