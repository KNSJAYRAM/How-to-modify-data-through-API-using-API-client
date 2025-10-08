## Modifying Data through API – Task Management App

This live practical session is your first step into building a real backend. You'll learn how to set up API routes in Express that allow users to modify data in a MongoDB database using Mongoose. You'll also test your APIs using an API client like Postman or Bruno.

Instead of recipes, let’s work on a simpler app: **Task Management**.

### 1. Scenario Overview

You're developing the backend for a basic **task manager**. Users should be able to:

- Add new tasks
- Update existing tasks
- Delete tasks

Each task has the following fields:

- `title` (String, required)
- `completed` (Boolean, default: false)

### 2. Plan Your API Endpoints

Define the routes needed to modify tasks:

| Endpoint            | Description         |
| ------------------- | ------------------- |
| POST `/tasks`       | Add a new task      |
| PUT `/tasks/:id`    | Update a task by ID |
| DELETE `/tasks/:id` | Delete a task by ID |

These routes should follow RESTful conventions.

### 3. Choose the Right Mongoose Methods

Use the appropriate Mongoose operations to handle data:

| Action | Mongoose Method            |
| ------ | -------------------------- |
| Create | `Task.create()`            |
| Update | `Task.findByIdAndUpdate()` |
| Delete | `Task.findByIdAndDelete()` |

### 4. Testing with API Client

Use Postman or Bruno to test your API:

- **POST**: Send `{"title": "Finish assignment"}` and expect status `201 Created`
- **PUT**: Update a task's `completed` status to `true`, expect status `200 OK`
- **DELETE**: Delete a task and expect status `204 No Content`

Make sure the database reflects the changes after each operation.

### 5. Repository and Setup Instructions

**Fork the StackBlitz Project:**

- A pre-configured link will be shared
- Fork and work on your own copy

**Push to GitHub:**
You can push manually or use StackBlitz’s GitHub integration.

**Manual Push Steps:**

```bash
git init
git remote add origin <your_repo_url>
git add .
git commit -m "Setup task API endpoints"
git push -u origin main
```

### 6. Submission Format

Submit a **PDF file** with the following:

- GitHub repository link
- Google Drive link to your video demo (ensure sharing is set to `kalvium.community`)
- A short note (1–2 lines) about your schema or API design

**Example PDF Naming Format:**
`task_api_<yourname>.pdf`

**Example Content:**

- GitHub: `https://github.com/<your_username>/task_api`
- Video: Google Drive link
- Note: “Created API routes for adding, updating, and deleting tasks using Mongoose methods.”
