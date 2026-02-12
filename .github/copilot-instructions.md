# AI Coding Agent Instructions

This document provides guidance for AI coding agents to be productive in this codebase. It outlines the architecture, workflows, conventions, and integration points specific to this project.

## Project Overview

This project appears to be a web application with the following structure:

- **`app.py`**: Likely the main entry point for the application.
- **`templates/`**: Contains HTML templates for rendering dynamic web pages.
- **`static/`**: Holds static assets like CSS files.
- **`jobs.csv`**: A CSV file, possibly used for storing or loading job-related data.

### Key Components

1. **Frontend**:
   - HTML templates in `templates/` follow a structure for different pages like login, signup, job listings, etc.
   - CSS for styling is located in `static/style.css`.

2. **Backend**:
   - `app.py` likely handles routing, business logic, and integration with the frontend.

3. **Data**:
   - `jobs.csv` may serve as a data source for job-related information.

### Data Flow
- User interactions on the frontend (e.g., login, signup) trigger backend routes in `app.py`.
- Backend processes data, potentially interacting with `jobs.csv`, and renders appropriate templates.

## Developer Workflows

### Running the Application
- Use Python to run the application. Example:
  ```bash
  python app.py
  ```

### Debugging
- Add debug logs in `app.py` to trace issues.
- Use browser developer tools to inspect frontend behavior.

## Project-Specific Conventions

- **HTML Templates**:
  - Templates are stored in `templates/` and follow a naming convention based on their purpose (e.g., `login.html`, `signup.html`).

- **Static Files**:
  - All static assets are stored in `static/`.

- **Data Storage**:
  - Job-related data is stored in `jobs.csv`. Ensure proper handling of file I/O operations.

## Integration Points

- **Frontend-Backend Communication**:
  - Backend routes in `app.py` render templates and handle form submissions.

- **External Dependencies**:
  - Ensure Python dependencies are installed. Use:
    ```bash
    pip install -r requirements.txt
    ```

## Examples

### Adding a New Route
To add a new route in `app.py`:
```python
from flask import render_template

@app.route('/new')
def new_route():
    return render_template('new_template.html')
```

### Modifying a Template
To add a new form in `templates/new_template.html`:
```html
<form action="/submit" method="POST">
    <input type="text" name="example" placeholder="Enter text">
    <button type="submit">Submit</button>
</form>
```

---

This document is a starting point. Update it as the project evolves.