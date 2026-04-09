# 1-1 Meeting Tracker (Employee Meeting Notes App)

A modern, lightweight **1-1 Meeting Tracker web application** built using **HTML, CSS, and JavaScript (Vanilla JS)**.

This app helps you manage employee meeting notes, track action items, and monitor completion status with a built-in dashboard — all directly in the browser.

---

# Live Features

## Meeting Management (CRUD)
- Add new meeting notes
- Edit existing notes
- Delete notes
- Auto-save using browser storage

---

## Dashboard (Real-time Insights)
The app includes a live dashboard showing:

- Total Meetings
- Completed Meetings
- Pending Meetings

The dashboard updates automatically whenever data changes.

---

## 🔍 Search Functionality
- Search meetings by **employee name**
- Instant filtering as you type

---

## Task Status Tracking
- Mark meetings as **Completed / Pending**
- Visual indicators for completed entries (strike-through style)
- Toggle completion anytime

---

## Persistent Storage
- Uses **localStorage (browser storage)**
- Data is saved automatically
- Entries remain available even after:
  - Page refresh
  - Browser restart
- No backend or database required

---

# How It Works

## Data Flow Architecture

1. User adds meeting details:
   - Employee name
   - Meeting date
   - Notes
   - Action items

2. Data is stored in:
   - JavaScript array (`entries[]`)

3. Data is persisted using:
   - `localStorage.setItem()`

4. On page load:
   - Data is retrieved using `localStorage.getItem()`

5. UI is dynamically rendered using:
   - DOM manipulation

---

# Tech Stack

| Layer      | Technology |
|------------|------------|
| Structure  | HTML5 |
| Styling    | CSS3 |
| Logic      | JavaScript (Vanilla JS) |
| Storage    | Browser LocalStorage |

---

# Dashboard Logic

The dashboard is computed dynamically:

- **Total** = all entries
- **Completed** = entries where `completed = true`
- **Pending** = Total - Completed

Example:
```javascript
Total: entries.length
Completed: entries.filter(e => e.completed).length
Pending: entries.filter(e => !e.completed).length

# How to Run Locally
- Clone the repository:
git clone https://github.com/rautelavivek/1-1-meeting-tracker.git

# Open project folder
Run: index.html

No installation or dependencies required

Key Functionalities
-  Edit Entry
- Click "Edit"
- Data loads into input fields
- Save updates existing record
- Delete Entry
Removes selected meeting permanently
- Complete Entry
- Toggles completion state
- Updates dashboard instantly
- UI Overview

Each entry contains:

- Employee Name
- Meeting Date
- Meeting Notes
- Action Items
- Status (Completed / Pending)

With action buttons:
- Edit
- Delete
- Complete / Undo
- Future Enhancements

Planned improvements:
- Calendar view of meetings
- Charts (visual dashboard analytics)
- Reminder notifications
- Cloud sync (Firebase / backend)
- Multi-user support
- Export to Excel / PDF
- Learning Outcomes

This project demonstrates:
- CRUD operations in frontend apps
- DOM manipulation in JavaScript
- State management using arrays
- Browser storage (localStorage)
- Real-time UI updates
- Basic dashboard analytics

Built as a learning project to demonstrate:
- Practical JavaScript skills
- Real-world mini SaaS-style app design
- Frontend state + storage handling

If you like this project:
- Star the repo
- Fork it
- Use it as a portfolio project
