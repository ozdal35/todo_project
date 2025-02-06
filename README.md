# Django To-Do List Project

A simple Django-based web application that allows users to manage their tasks. Users can register, log in, create tasks, update tasks, mark tasks as completed, and delete tasks.

## Features

- **User Authentication:**
  - Registration using Django’s built-in `UserCreationForm`.
  - Login and logout functionality.
  - Redirect to login page immediately after logout.

- **Task Management:**
  - Create new tasks.
  - View a list of tasks (only tasks belonging to the logged-in user).
  - Edit/update tasks.
  - Delete tasks.

- **Responsive Design:**
  - Integrated CSS styling for a modern, visually appealing interface.
  - Responsive design for mobile and desktop browsers.

## Requirements

- Python 3.8+ (or your preferred Python version)
- Django 5.1.6 (or your current Django version)
- SQLite (default database, configured in settings)

## Installation

1. **Clone the repository:**

   ```bash
   git clone <repository_url>
   cd django-todo-project
   ```
   
2. **Create a virtual environment:**

   ```bash
   python -m venv env
   ```
   
3. **Activate the virtual environment:**

  ```bash
  env\Scripts\activate
  ```

4. **Install the required packages:**

  ```bash
  pip install django
  ```

5. **Apply migrations:**

  ```bash
 python manage.py makemigrations
 python manage.py migrate
  ```

6. **Create a superuser (optional, for admin access):**

  ```bash
  python manage.py createsuperuser
  ```

7. **Run the development server:**

  ```bash
  python manage.py runserver
  ```

8.**Open your browser and navigate to: http://127.0.0.1:8000/register**


Usage
Register:
Navigate to /register/ to create a new account.

Login:
Log in at /login/.

Manage Tasks:
Once logged in, you will be redirected to the task list where you can:

Create new tasks by clicking "Create New Task".
Edit or update tasks using the Edit button.
Delete tasks using the Delete button.
Logout (the logout URL automatically redirects you to the login page).
Customization
CSS Styling:
Customize the appearance by editing the tasks/static/tasks/style.css file.

Templates:
Modify templates in the templates/ directory to change the UI and layout.

Troubleshooting
Logout Redirection:
Ensure your URL configuration for logout is set up to immediately redirect to the login page. For example, in todo_project/urls.py:
``path('logout/', auth_views.LogoutView.as_view(next_page='/login/'), name='logout'),``
Static Files:
Make sure your STATIC_URL is correctly set in settings.py and that your static files are located in the proper directories.





