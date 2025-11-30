Employee Attendance System (MERN)

A web-based Attendance Tracking System with two roles: Employee and Manager.

Employees can mark attendance, and managers can monitor team activity, view reports, and analyze attendance trends.

📌 1. Features Overview
👨‍💼 Employee Features

Register and Login

Mark Check-In / Check-Out

View my attendance history

Monthly summary (Present, Absent, Late)

Dashboard with quick stats

🧑‍💼 Manager Features

Login

View attendance of all employees

Filter by employee, date, status

Team attendance summary

Export CSV reports

Dashboard with graphs & insights

🛠 2. Tech Stack
Frontend

React.js

Redux Toolkit / Zustand

HTML5, CSS3

Backend

Node.js

Express.js

Database

MongoDB (recommended)

🗄️ 3. Database Schema (Simple View)
🧍 Users Collection

id

name

email

password

role (employee / manager)

employeeId

department

createdAt

📅 Attendance Collection

id

userId

date

checkInTime

checkOutTime

status

totalHours

createdAt


4. API Endpoints
Auth

POST /api/auth/register

POST /api/auth/login

GET /api/auth/me

Employee Attendance

POST /api/attendance/checkin

POST /api/attendance/checkout

GET /api/attendance/my-history

GET /api/attendance/my-summary

GET /api/attendance/today

Manager Attendance

GET /api/attendance/all

GET /api/attendance/employee/:id

GET /api/attendance/summary

GET /api/attendance/export

GET /api/attendance/today-status

Dashboards

GET /api/dashboard/employee

GET /api/dashboard/manager

📊 5. Dashboard Requirements
Employee Dashboard

Today's attendance status

Monthly stats

Total hours worked

Recent attendance list

Quick Check-In/Out button

Manager Dashboard

Total employees

Present / Absent today

Late arrivals

Weekly trends chart

Department-based chart

Absent employees list



⚙️ 6. How to Run the Project
Backend Setup
cd backend
npm install
npm run dev


Frontend Setup
cd frontend
npm install
npm start

🔐 7. Environment Variables (.env)

PORT=5000
MONGO_URI=your_mongo_url
JWT_SECRET=your_secret

📦 8. Folder Structure (Clean & Clear)

This is the final folder structure you should show in README (simple & understandable).

Employee-Attendance-System/
│
├── backend/
│   ├── controllers/
│   ├── middleware/
│   ├── models/
│   ├── routes/
│   ├── config/
│   ├── server.js
│   └── .env
│
├── frontend/
│   ├── src/
│   │   ├── app/            # Redux store or Zustand store
│   │   ├── components/     # Reusable components
│   │   ├── pages/          # Screens (Employee + Manager)
│   │   ├── features/       # Slices or stores
│   │   └── index.js
│   └── package.json
│
└── README.md

🤝 9. Contributing

Fork

Create branch

Submit PR


📬 10. Feedback

Suggestions and improvements are welcome!







