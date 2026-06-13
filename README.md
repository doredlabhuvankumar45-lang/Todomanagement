# Todomanagement
📝 Spring Boot Todo Management App

A modern Full-Stack Todo Management Application developed using Spring Boot, Java 21, Spring Data JPA, Hibernate, H2 Database, HTML5, CSS3, and JavaScript. The application enables users to efficiently manage daily tasks through a responsive interface while providing secure authentication, task prioritization, due-date tracking, filtering, and search functionality.

📌 Project Overview

Managing personal and professional tasks effectively is essential in today's fast-paced world. This project provides a centralized platform where users can create, organize, prioritize, update, and monitor tasks in real time.

The application follows a client-server architecture with a responsive frontend and a robust Spring Boot backend connected through RESTful APIs.

Key Objectives
Develop a responsive task management system.
Implement secure user authentication.
Enable task CRUD operations.
Support task prioritization and categorization.
Provide filtering and search capabilities.
Maintain normalized database design.
Ensure scalability and maintainability through layered architecture.
🚀 Features
👤 User Management
User Registration
User Login
Session Management
User-specific Task Access
Authentication Validation
✅ Task Management
Create New Tasks
View All Tasks
Update Existing Tasks
Delete Tasks
Mark Tasks as Completed
Toggle Completion Status
📅 Task Organization
Due Date Tracking
Priority Levels (High, Medium, Low)
Category Assignment
Task History Tracking
🔍 Search & Filter
Filter by Status
Filter by Priority
Search by Title
Search by Description
📊 Dashboard
Total Tasks Count
Completed Tasks Count
Pending Tasks Count
Real-Time Updates
📱 Responsive Design
Desktop Support
Tablet Support
Mobile Support
🛠️ Technology Stack
Frontend
Technology	Purpose
HTML5	Page Structure
CSS3	Styling & Layout
JavaScript ES6	Client-Side Logic
Font Awesome	Icons
Google Fonts	Typography
Backend
Technology	Purpose
Java 21	Programming Language
Spring Boot 3.5.11	Backend Framework
Spring Data JPA	Data Access Layer
Hibernate ORM	Object Relational Mapping
H2 Database	Development Database
Lombok	Boilerplate Reduction
Maven	Dependency Management
Development Tools
IntelliJ IDEA
Visual Studio Code
Postman
MySQL Workbench
Git & GitHub
🏗️ System Architecture
+--------------------+
|     Frontend       |
| HTML CSS JavaScript|
+---------+----------+
          |
          | REST API
          v
+--------------------+
|   Spring Boot API  |
+---------+----------+
          |
          v
+--------------------+
|   Service Layer    |
+---------+----------+
          |
          v
+--------------------+
| Repository Layer   |
+---------+----------+
          |
          v
+--------------------+
| H2 / MySQL Database|
+--------------------+
📂 Project Structure
todo-management-app
│
├── src
│   ├── main
│   │   ├── java
│   │   │   ├── controller
│   │   │   ├── service
│   │   │   ├── repository
│   │   │   ├── model
│   │   │   ├── dto
│   │   │   └── TodoManagementApplication.java
│   │   │
│   │   └── resources
│   │       ├── application.properties
│   │       └── data.sql
│   │
│   └── test
│
├── frontend
│   ├── index.html
│   ├── login.html
│   ├── register.html
│   ├── dashboard.html
│   ├── style.css
│   └── app.js
│
├── pom.xml
└── README.md
🗄️ Database Design

The database follows Third Normal Form (3NF) and consists of five related tables.

Users

Stores account information.

Column
id
username
email
password
full_name
created_at
updated_at
Priorities

Stores predefined priority levels.

Column
priority_id
level
value
color_code
Categories

Stores task categories.

Column
category_id
name
description
color_code
user_id
Todos

Stores task information.

Column
todo_id
title
description
due_date
completed
user_id
category_id
priority_id
Task History

Maintains audit logs.

Column
history_id
todo_id
user_id
action_type
changed_at
🔗 REST API Endpoints
Authentication APIs
Register User
POST /api/auth/register
Login User
POST /api/auth/login
Todo APIs
Get User Tasks
GET /api/todos/user/{userId}
Filter by Status
GET /api/todos/user/{userId}/status
Filter by Priority
GET /api/todos/user/{userId}/priority/{priorityId}
Get Tasks Due Between Dates
GET /api/todos/user/{userId}/due
Create Task
POST /api/todos/user/{userId}
Update Task
PUT /api/todos/{todoId}
Toggle Status
PATCH /api/todos/{todoId}/toggle
Delete Task
DELETE /api/todos/{todoId}
⚙️ Installation Guide
Clone Repository
git clone https://github.com/yourusername/todo-management-app.git
cd todo-management-app
Build Project
mvn clean install
Run Application
mvn spring-boot:run

Backend runs at:

http://localhost:8080
Access H2 Database Console
http://localhost:8080/h2-console

Default configuration:

JDBC URL: jdbc:h2:mem:testdb
Username: sa
Password:
🖥️ Application Screens
Landing Page
Application Introduction
Feature Highlights
Registration & Login Navigation
Login Page
Email Authentication
Form Validation
Session Creation
Registration Page
User Account Creation
Password Validation
Terms Acceptance
Dashboard
Task Creation
Task Listing
Filtering
Statistics
Edit Modal
🔄 Application Workflow
Authentication Flow
User Login
     ↓
Frontend Validation
     ↓
POST Request
     ↓
Spring Boot Authentication
     ↓
Database Verification
     ↓
Session Creation
     ↓
Dashboard Access
Task Creation Flow
Create Task
     ↓
Frontend Validation
     ↓
POST API Request
     ↓
Backend Validation
     ↓
Database Storage
     ↓
Response Returned
     ↓
Dashboard Updated
🧪 Testing
Unit Testing
Form Validation
Search Functions
Date Formatting
Integration Testing
API Endpoints
Authentication Flow
CRUD Operations
UI Testing
Chrome
Firefox
Edge
Functional Testing
Registration
Login
Task Creation
Task Editing
Task Deletion
Filtering
Search
Performance Testing
Fast API Response
Efficient Task Rendering
🔒 Security Features
User-specific Data Access
Authentication Validation
Form Validation
Input Sanitization
Error Handling
Data Integrity Constraints
📈 Future Enhancements
Short-Term
JWT Authentication
BCrypt Password Encryption
Email Notifications
File Attachments
Custom Categories
Medium-Term
Recurring Tasks
Team Collaboration
Mobile Applications
CSV/PDF Export
Dark Mode
Long-Term
Cloud Deployment
Real-Time Synchronization
AI Task Suggestions
Google Calendar Integration
Analytics Dashboard
Technical Improvements
Unit Test Coverage
Swagger Documentation
Docker Containerization
Redis Caching
Performance Optimization
🎯 Learning Outcomes

Through this project, the following skills were developed:

Full Stack Web Development
Spring Boot Development
REST API Design
Database Modeling
Hibernate ORM
Frontend Development
Debugging & Testing
Git Version Control
Software Documentation
👨‍💻 Author

D. Bhuvan kumar
Roll No: 22NE1A0429

📄 License

This project is developed for academic and educational purposes. Feel free to use and modify it for learning and research purposes.
