# 🏠 HomeBase — Periodic Home Task Tracker

## Elevator Pitch
HomeBase is a simple, collaborative web application that helps households keep track of recurring home maintenance tasks—like **changing air filters**, cleaning dryer vents, testing smoke detectors, and replacing water filters—so nothing gets forgotten. By centralizing periodic tasks and showing real-time updates when tasks are completed, HomeBase turns home maintenance into an easy, shared routine.

---

## Key Features
- 📅 Create and manage **recurring home tasks**
  - Examples: **change HVAC air filter**, clean gutters, test smoke detectors
- 🔔 View upcoming and overdue tasks
- 👥 Shared household task list
- 📊 Task completion history
- ⚡ Real-time updates when tasks are completed
- 🔐 Secure login with persistent storage

---

## Technology Specification

### HTML
- Semantic HTML for structure and accessibility
- Core views:
  - Login / Register
  - Dashboard
  - Task Detail View
- Forms for adding, editing, and completing tasks

### CSS
- Responsive design for desktop and mobile
- Clean layout with consistent spacing and color contrast
- Simple animations for task completion and status changes

### React
- Single Page Application built with React
- Component-based architecture:
  - `LoginForm`
  - `TaskCard`
  - `TaskList`
  - `AddTaskModal`
  - `TaskDetail`
  - `ActivityFeed`
- React Router used for navigation
- UI reacts dynamically to user actions and server responses

### Backend Service
Node.js backend providing REST endpoints for:

**Authentication**
- Register
- Login
- Logout

**Task Management**
- Create recurring tasks
- Retrieve upcoming and overdue tasks
- Mark tasks as completed
- Fetch task completion history

**Third-Party API**
- Simple public API call to display a **home maintenance tip**
  - Example: “Tip: Replace HVAC air filters every 1–3 months.”
- No authentication required

### Database
Persistent storage for:
- Users
- Households
- Tasks (name, frequency, next due date)
- Task completion history

### WebSocket
- Real-time updates sent from server to clients:
  - When a task is completed by any household member
  - Live household activity feed updates without page refresh

### Infrastructure
- Application deployed using AWS
- HTTPS enabled
- DNS configured
- Code managed with GitHub

### Security and Design Practices
- Passwords securely hashed
- Auth-protected routes
- Input validation on client and server
- HTTPS-only communication

---

## Rough Design Sketches

> Sketches created using NinjaMock / Google Docs and embedded below.

### Login / Register
![Login Sketch](docs/login-sketch.png)

### Dashboard
![Dashboard Sketch](docs/dashboard-sketch.png)

### Task Detail View
![Task Detail Sketch](docs/task-detail-sketch.png)

---

## Example User Flow
1. User registers and creates a household.
2. User adds a recurring task: **“Change HVAC air filter”** every 60 days.
3. Dashboard shows upcoming and overdue tasks.
4. When a task is completed, all household members see the update in real time.

---

## Deliverable Scope
This README contains only the **startup specification** required for this deliverable.
