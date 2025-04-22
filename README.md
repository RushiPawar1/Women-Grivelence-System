# Women-Grivelence-System
🌸 Women Grievance Redressal System is a secure web app that empowers women to confidentially register and track grievances. Designed for institutions and workplaces, it ensures transparency in addressing harassment, discrimination, or misconduct, offering a safe platform for complaint submission and resolution.
A secure and confidential web application that enables women to register and track grievances in institutions or workplaces. The platform supports user/admin roles, complaint tracking, and email notifications.

---

## 🚀 Features

- User/Admin Authentication
- Complaint Registration and Tracking
- Status Update and Admin Dashboard
- Email Alerts (NodeMailer)
- Secure & Responsive Design

---

## 🛠️ Tech Stack

- **Frontend:** HTML, CSS, JavaScript
- **Backend:** Node.js, Express.js
- **Database:** MySQL
- **Email Service:** NodeMailer

---

## 🔗 Database Setup

1. **Create Database**
   ```sql
   CREATE DATABASE women_grievance;
Create Tables

Example table structure (simplify as per your needs):

sql
Copy
Edit
CREATE TABLE users (
  id INT AUTO_INCREMENT PRIMARY KEY,
  name VARCHAR(100),
  email VARCHAR(100) UNIQUE,
  password VARCHAR(255),
  role ENUM('user', 'admin') DEFAULT 'user'
);

CREATE TABLE complaints (
  id INT AUTO_INCREMENT PRIMARY KEY,
  user_id INT,
  category VARCHAR(100),
  description TEXT,
  status ENUM('Pending', 'Under Review', 'Resolved') DEFAULT 'Pending',
  created_at TIMESTAMP DEFAULT CURRENT_TIMESTAMP,
  FOREIGN KEY (user_id) REFERENCES users(id)
);
Update DB Credentials

Open the .env file or config/db.js and set your database credentials:

env
Copy
Edit
DB_HOST=localhost
DB_USER=root
DB_PASSWORD=yourpassword
DB_NAME=women_grievance
📦 Installation
bash
Copy
Edit
git clone https://github.com/yourusername/women-grievance-system.git
cd women-grievance-system
npm install
▶️ Run the App
bash
Copy
Edit
npm start
Then visit: http://localhost:3000

📧 Email Configuration (NodeMailer)
Update .env with email credentials:

env
Copy
Edit
EMAIL_USER=your_email@gmail.com
EMAIL_PASS=your_email_password
