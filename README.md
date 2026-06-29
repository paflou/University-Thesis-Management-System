# University Thesis Management System

A centralized platform designed to streamline the lifecycle of academic thesis projects. This system facilitates coordination between students, professors, and administrative staff, replacing manual tracking with a digital, role-based workflow.

## Key Features
* **Role-Based Access Control:** Distinct interfaces and permission sets for students, faculty, and administrative secretaries.
* **Thesis Lifecycle Management:** End-to-end handling of thesis assignment, proposal approval, grading, and presentation scheduling.
* **Data Integrity:** Structured database schema ensures consistent tracking of project data across multiple semesters.
* **Automated Data Handling:** Includes support for database seeding to quickly initialize testing environments.

## Technical Stack
* **Backend:** Node.js, Express.js
* **Database:** MariaDB
* **Frontend:** HTML5, CSS3, Bootstrap 5, JavaScript (Vanilla/ES6)
* **Development Tools:** nodemon, npm

## Architecture
The backend follows a layered architecture separating HTTP request handling from business logic and data access.

- **Routes:** Define REST endpoints and route incoming requests.
- **Controllers:** Validate requests and coordinate application logic.
- **Services:** Implement business rules for thesis management, user roles, grading, and approvals.
- **Middleware:** Enforce authentication, authorization, and file upload validation.
- **Database:** MariaDB relational schema with SQL-based initialization and seeding.

# Setup Instructions

## Prerequisites
* Node.js installed on your machine.
* A running MySQL or MariaDB instance.

## 1. Create a `.env` file

Create a `.env` file in the root directory of the project and add your MariaDB database credentials in the following format:
```bash
DB_HOST=localhost
DB_USER=root
DB_PASSWORD=your_root_password
DB_NAME=diplomaDB
DB_CONNECTION_LIMIT= 5
```

## 2. Install dependencies and seed the database

Run the following command to install node modules:

```bash
npm install
```

Create a mariaDB database with the name diplomaDB
```
CREATE DATABASE diplomaDB;
```

Run the following command to seed the database with initial data:

```bash
npm run seed
```
## 3. Start the server

Start the server by running:
```bash
npm start
```

## 4. Access the application

Open your browser and go to:

```bash
http://localhost:3000
```

If you want to run the server in development mode with automatic reload on code changes, use:

```bash
npm run dev
```

## Future Enhancements:
* **OAuth Integration:** Implement SSO for university-wide logins.
* **Dashboard Analytics:** Add visual reporting for administrators to track department thesis progress.
* **Real-time Notifications:** Implement WebSockets for status updates regarding thesis approvals.
