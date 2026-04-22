# Overview testing

The system is a web-based todo management application that allows users to create, organize, and track personal tasks efficiently. It provides a clean, intuitive interface for managing daily work, personal goals, and projects through structured task lists with categorization and deadline tracking.

The application targets individual users who need a reliable, lightweight tool to stay organized. Users can register for a personal account, and all their data is private and isolated from other users. The system supports full task lifecycle management — from creation through completion — with support for categories and due dates to help users prioritize effectively.

The application is accessible via any modern web browser with no installation required. Authentication ensures that each user's tasks are secure and only visible to them. The overall approach favors simplicity and speed, enabling users to capture and manage tasks with minimal friction.

---

# Capabilities

## User Authentication

- Users can register for a new account by providing a unique email address and a password.
- Users can log in to their account using their registered email and password.
- Users can log out of their account, ending their session immediately.
- Passwords must be at least 8 characters long and stored securely (never in plain text).
- Unauthenticated users are redirected to the login page when attempting to access protected content.
- Users can request a password reset via a link sent to their registered email address.
- Each user's data is fully isolated; no user can view or modify another user's tasks.

## Task Management (CRUD)

- Authenticated users can create a new task by providing at minimum a title.
- Users can optionally add a description when creating or editing a task.
- Users can view a list of all their tasks in a single, consolidated view.
- Users can view the full details of an individual task on a dedicated detail view.
- Users can edit any field of a task they own (title, description, category, due date, status).
- Users can delete a task they own; deletion is permanent and requires a confirmation step.
- Users can mark a task as complete or incomplete using a single action (e.g., checkbox or toggle).
- Each task records the date and time it was created and last updated.

## Categories

- Users can create custom categories with a name to organize their tasks.
- Users can assign one category to a task at the time of creation or during editing.
- Users can view all tasks belonging to a specific category via a filtered view.
- Users can rename an existing category; all tasks assigned to it reflect the updated name.
- Users can delete a category; tasks previously assigned to it become uncategorized.
- A default "Uncategorized" state exists for tasks with no assigned category.

## Due Dates

- Users can assign an optional due date (date and time) to any task.
- Tasks with due dates are visually distinguished from tasks without due dates.
- Tasks that are past their due date and not yet complete are visually flagged as overdue.
- Users can filter or sort their task list by due date (earliest first, latest first).
- Users can clear a due date from a task, making it open-ended.

## Task Filtering &amp; Sorting

- Users can filter their task list by status: All, Active (incomplete), or Completed.
- Users can filter tasks by category.
- Users can sort tasks by creation date, due date, or title (ascending and descending).
- Users can search tasks by keyword, matching against task titles and descriptions.
- Active filters and sort preferences are preserved within a user session.

## User Interface &amp; Experience

- The application is fully usable on desktop and mobile browsers (responsive layout).
- Task list updates (create, complete, delete) are reflected immediately without a full page reload.
- The application provides clear error messages for invalid inputs (e.g., empty title, invalid date).
- Confirmation is required before any destructive action (task deletion, category deletion).

## Security &amp; Performance

- All communication between the user's browser and the server is encrypted (HTTPS).
- User sessions expire after a defined period of inactivity (maximum 30 days for remembered sessions, 24 hours otherwise).
- The task list for any user loads within 2 seconds under normal network conditions.
- The application handles up to 500 tasks per user without degradation in list load time.
- Input fields are protected against common injection attacks (e.g., XSS, SQL injection).

