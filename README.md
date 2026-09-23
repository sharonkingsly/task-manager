# Student Task Manager

A simple full-stack mini project to add, complete, and delete daily tasks.

## Tech Stack
- **Backend:** Python (Flask)
- **Database:** SQLite
- **Frontend:** HTML, CSS, Jinja2 templates

## How to Run
1. Install Flask:
   ```
   pip install -r requirements.txt
   ```
2. Start the app:
   ```
   python app.py
   ```
3. Open your browser to:
   ```
   http://127.0.0.1:5000
   ```

A file called `tasks.db` will be created automatically on first run — that's your SQLite database.

## Project Structure
```
task_manager/
├── app.py              # Flask backend: routes + database logic
├── templates/
│   └── index.html       # Main page (Jinja2 template)
├── static/
│   └── style.css        # Styling
├── requirements.txt
└── README.md
```

## How It Works (for explaining in an interview)
- **Routes:**
  - `GET /` → loads all tasks from the database and displays them
  - `POST /add` → reads the task title from the submitted form and inserts it into the database
  - `GET /complete/<id>` → flips a task's `is_done` status between 0 and 1
  - `GET /delete/<id>` → removes a task by its ID
- **Database:** one table, `tasks`, with columns `id`, `title`, `is_done`
- **Frontend:** Jinja2 loops through the tasks list from the backend and renders each row; CSS handles the styling and strikethrough effect for completed tasks

## Possible Ways to Extend It
- Add user login so each student has their own task list
- Add due dates and sort by urgency
- Add categories/tags for tasks
- Convert to a REST API (Flask + JSON) and build a separate JS frontend
- Deploy it using Render, Railway, or PythonAnywhere

## Why This Project Is Good to Talk About
It touches the core full-stack concepts: routing, handling form data, reading/writing to a database, and rendering dynamic HTML — enough to explain confidently, and easy to extend live if an interviewer asks "can you add a feature right now?"
