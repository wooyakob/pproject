# pproject

I will start with this: 

If using Django, the application built during this week's workshop can serve as a starting point
A simple task manager for users to manage their tasks.

What are the various features you would like your project to offer? 

User Authentication: Allow users to register, log in, and log out.
Task Management: Allow users to create, view, update, and delete tasks.
Task Status: Each task can have a status of "Pending," "In Progress," or "Completed."
What are the API endpoints that you would need to set up for each feature? List them along with the respective HTTP verb, endpoint URL, and any special details (query parameters, request bodies, headers). 

User Authentication:

POST /api/register: Register a new user. (Request body: username, email, password)
POST /api/login: Log in an existing user. (Request body: username, password)
POST /api/logout: Log out the currently logged-in user. (No request body)
Task Management:

GET /api/tasks: Retrieve all tasks for the currently logged-in user. (No request body)
POST /api/tasks: Create a new task for the currently logged-in user. (Request body: title, description, status)
GET /api/tasks/{task_id}: Retrieve a specific task by its ID. (No request body)
PUT /api/tasks/{task_id}: Update a specific task by its ID. (Request body: title, description, status)
DELETE /api/tasks/{task_id}: Delete a specific task by its ID. (No request body)
Provide a description of the database tables required for your application, including column names, data types, constraints, and foreign keys. Include your database name. You can optionally include an ER diagram.



Table: User

Columns: id (Primary Key), username (Unique), email, password
Table: Task

Columns: id (Primary Key), title, description, status, user_id (Foreign Key to User table)
