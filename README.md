# S S SUCCESS MISSION — Professional Website + Admin Panel

A self-contained working demo built for **S S SUCCESS MISSION**.
## Included
- Premium responsive public website
- Hero/campus image using the supplied school photo
- Programs, About, Teachers, Campus, Playground/Gallery, Future Plan
- Admission enquiry form
- Admin login + dashboard
- Admission enquiry management/status
- Student register
- Daily attendance (Present/Absent)
- Teacher profiles with photo upload, qualification, role and bio
- Gallery/playground photo upload
- School settings / future plan editor
- JSON export for admission enquiries
- Data persists in browser localStorage
## Run
Option 1: Open `index.html` directly in a modern browser.

Option 2 (recommended): from this folder run:

```bash
python -m http.server 8080
```
Then open `http://localhost:8080`.

## Important
This is a **working frontend/management system**, not a production multi-user server. Data is stored in the browser. For production, connect the same UI to a secure backend/database (MySQL/PostgreSQL/Supabase/Firebase), real authentication, cloud file storage, backups, WhatsApp/email notifications and role-based permissions.

S-S-SUCCESS-MISSION/
│
├── index.html              # Public website
├── admin.html              # Admin login + dashboard
├── style.css               # Complete responsive styling
├── app.js                  # Public website functionality
├── admin.js                # Admin functionality
│
├── assets/
│   ├── school-front.png
│   ├── teacher-1.jpg
│   ├── teacher-2.jpg
│   └── gallery/
│       ├── playground.jpg
│       ├── classroom.jpg
│       └── campus.jpg
│
└── README.md

Admin Login
     ↓
Dashboard
     ├── Admission Enquiries
     │      ├── View
     │      ├── Status
     │      └── Export JSON
     │
     ├── Students
     │      ├── Add Student
     │      └── Delete Student
     │
     ├── Attendance
     │      ├── Select Date
     │      ├── Present
     │      ├── Absent
     │      └── Save
     │
     ├── Teachers
     │      ├── Add Profile
     │      ├── Photo
     │      ├── Qualification
     │      ├── Role
     │      └── Bio
     │
     ├── Gallery
     │      ├── Upload Photo
     │      └── Delete Photo
     │
     └── Settings
            ├── School Name
            ├── Phone
            ├── Location
            └── Future Plan

            index.html
     │
     ├── app.js
     │
     └── localStorage
            ↑
            │
admin.html


│
     └── admin.js                      ┌─────────────────┐
                    │ Public Website  │
                    └────────┬────────┘
                             │
                    ┌────────▼────────┐
                    │   FastAPI API   │
                    └────────┬────────┘
                             │
          ┌──────────────────┼──────────────────┐
          │                  │                  │
   ┌──────▼──────┐    ┌──────▼──────┐    ┌──────▼──────┐
   │ PostgreSQL  │    │ File Storage│    │ Notifications│
   │  Database   │    │   Photos    │    │ WhatsApp/Email│
   └─────────────┘    └─────────────┘    └──────────────┘
                             │
                    ┌────────▼────────┐
                    │ Admin Dashboard │
                    └─────────────────┘# SSSUCCESS.MISSION
