# Club Management System - Backend

This is the backend for the **Club Management System**, developed with **Node.js**, **Express.js**, and **MySQL**. The system is designed to centralize club registrations and management for **NIT Warangal**, providing a streamlined platform for both students and administrators.

## Description

The **Club Management System** aims to simplify and centralize the process of managing clubs, events, and student registrations at **NIT Warangal**. This platform offers a user-friendly interface for students to register for clubs and view upcoming events and notices. Administrators can easily manage club activities, post notices, and track achievements.

### Key Objectives:

- **Centralized Management**: Unify all club-related activities under a single platform.
- **Simplified Registration**: Allow students to register for clubs and events with ease.
- **Admin Tools**: Provide an intuitive dashboard for club coordinators to manage their respective clubs.
- **Event and Notice Board**: Share updates, event details, and important notices in real-time.

## Features

- Club and student registration
- Admin dashboard for managing clubs, events, notices, and achievements
- Secure session management
- File uploads using `multer`

## Tech Stack

- **Backend**: Node.js, Express.js
- **Database**: MySQL
- **View Engine**: EJS
- **Middleware**: `body-parser`, `express-session`, `multer`

## Prerequisites

- [Node.js](https://nodejs.org/)
- [MySQL](https://www.mysql.com/)

## Installation

1. Clone the repo:

   ```bash
   git clone https://github.com/yourusername/club-management-backend.git
   cd club-management-backend
   ```

2. Install dependencies:

   ```bash
   npm install
   ```

3. Set up the database:

   - Create a MySQL database named `PROJECT`.
   - Import the necessary SQL scripts to create tables.

4. Update the database configuration in `app.js`:

   ```javascript
   var con = mysql.createConnection({
     host: "localhost",
     user: "root",
     password: "root",
     database: "PROJECT",
   });
   ```

5. Start the server:

   ```bash
   node app.js
   ```

6. Open [http://localhost:4000](http://localhost:4000) in your browser.

## Project Structure

## Routes

### Public Routes

- `/` - Home page listing clubs
- `/about` - About page
- `/club-registration` - Club registration form
- `/student_registration` - Student registration form

### Admin Routes

- `/admin/auth` - Admin login
- `/admin/dashboard/:id` - Admin dashboard for club management

### API Routes

- `POST /student_registration` - Register a new student
- `POST /club-registration` - Register a new club
- `POST /admin/dashboard/:id/notice` - Submit a notice
- `POST /admin/dashboard/:id/event` - Submit an event
- `POST /admin/dashboard/:id/achievements` - Submit an achievement

## Credits

Developed and maintained by:

- **Yash Paunikar**
- **Varun Haralaka**

## License

This project is licensed under the MIT License. See `LICENSE` for details.
