Employee Attendance System — MERN

A complete attendance tracking platform with Employee and Manager roles.
Employees can mark attendance daily, while Managers can view and manage team attendance with dashboards, filtering, and reporting.

🚀 Tech Stack
Frontend

React.js

Redux Toolkit / Zustand

HTML5, CSS3, JavaScript

Backend

Node.js

Express.js

Database

MongoDB (or PostgreSQL if preferred)

📌 Features
👨‍💼 Employee Features

Register / Login

Check In / Check Out

View attendance history (table or calendar)

Monthly summary (Present / Absent / Late / Half-Day)

Dashboard with quick stats

Profile page

🧑‍💼 Manager Features

Login

View all employees' attendance

Filter by employee, date, status

Team attendance summary

Export attendance as CSV

Dashboard with team statistics

Team calendar view

📁 Project Structure
Employee-Attendance-System/
│
├── backend/
│   ├── controllers/
│   │   ├── authController.js
│   │   ├── attendanceController.js
│   │   └── dashboardController.js
│   ├── middleware/
│   │   └── authMiddleware.js
│   ├── models/
│   │   ├── User.js
│   │   └── Attendance.js
│   ├── routes/
│   │   ├── authRoutes.js
│   │   ├── attendanceRoutes.js
│   │   └── dashboardRoutes.js
│   ├── config/
│   │   └── db.js
│   ├── .env
│   └── server.js
│
├── frontend/
│   ├── src/
│   │   ├── app/
│   │   │   └── store.js
│   │   ├── features/
│   │   │   ├── authSlice.js
│   │   │   └── attendanceSlice.js
│   │   ├── pages/
│   │   │   ├── EmployeeDashboard.jsx
│   │   │   ├── ManagerDashboard.jsx
│   │   │   ├── Login.jsx
│   │   │   ├── Register.jsx
│   │   │   ├── MyAttendance.jsx
│   │   │   └── Reports.jsx
│   │   ├── components/
│   │   │   ├── Navbar.jsx
│   │   │   └── CalendarView.jsx
│   │   └── index.js
│   ├── package.json
│   └── README.md

🗄️ Database Schema
Users
Field	Description
id	Unique identifier
name	Employee name
email	Login email
password	Hashed password
role	employee / manager
employeeId	Unique employee code
department	Department name
createdAt	Timestamp
Attendance
Field	Description
id	Unique identifier
userId	Reference to User
date	Attendance date
checkInTime	Time of check-in
checkOutTime	Time of check-out
status	present / absent / late / half-day
totalHours	Calculated hours
createdAt	Timestamp
🔗 API Endpoints
Auth
POST /api/auth/register
POST /api/auth/login
GET  /api/auth/me

Employee Attendance
POST /api/attendance/checkin
POST /api/attendance/checkout
GET  /api/attendance/my-history
GET  /api/attendance/my-summary
GET  /api/attendance/today

Manager Attendance
GET /api/attendance/all
GET /api/attendance/employee/:id
GET /api/attendance/summary
GET /api/attendance/export
GET /api/attendance/today-status

Dashboards
GET /api/dashboard/employee
GET /api/dashboard/manager

📊 Dashboard Requirements
Employee Dashboard

Today’s status (Checked In / Not Checked In)

Present / Absent / Late statistics for this month

Total hours worked

Recent 7-day attendance

Quick Check-In / Check-Out button

Manager Dashboard

Total employees

Today’s present / absent count

Late arrivals

Weekly attendance chart

Department-wise attendance chart

List of absent employees

⚙️ Environment Variables (.env)
PORT=5000
MONGO_URI=your_mongo_db_url
JWT_SECRET=your_secret_key

🚀 Setup Instructions
Backend
cd backend
npm install
npm run dev

Frontend
cd frontend
npm install
npm start


Visit: http://localhost:3000

📦 Export Reports

Managers can export attendance in CSV format.

🤝 Contributing

Fork the repository

Create a branch

Submit a PR
