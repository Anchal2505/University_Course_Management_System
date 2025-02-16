# University_Course_Management_System

# Overview

The University Course Management System is a Spring Boot-based RESTful API designed to manage students, instructors, courses, assignments, and user authentication.

# Tech Stack

1. Spring Boot (Spring Web, Spring Data JPA, Spring DevTools)

2. MySQL (Database)

3. JPA/Hibernate (ORM for database interactions)

4. Maven (Dependency management)

# Project Setup

# Prerequisites

Java 17+

Spring Boot

MySQL Server

Eclipse

# Steps to Run the Project

1. Clone the repository:

    git clone <repository-url>
    
    cd university-course-management

2. Configure MySQL Database in application.properties:

    spring.datasource.url=jdbc:mysql://localhost:3306/university_db
   
    spring.datasource.username=root
   
    spring.datasource.password=yourpassword
   
    spring.jpa.hibernate.ddl-auto=update
   
    spring.jpa.show-sql=true

4. Build and run the project:

    mvn spring-boot:run

# API Endpoints

# Admin Endpoints

# Student Management

GET /api/admin/students - Retrieve all students

GET /api/admin/students/{studentId} - Retrieve student details

POST /api/admin/students - Create a new student

PUT /api/admin/students/{studentId} - Update student details

DELETE /api/admin/students/{studentId} - Delete a student

# Instructor Management

GET /api/admin/instructors - Retrieve all instructors

GET /api/admin/instructors/{instructorId} - Retrieve instructor details

POST /api/admin/instructors - Create a new instructor

PUT /api/admin/instructors/{instructorId} - Update instructor details

DELETE /api/admin/instructors/{instructorId} - Delete an instructor

# Course Management

GET /api/admin/courses - Retrieve all courses

GET /api/admin/courses/{courseId} - Retrieve course details

POST /api/admin/courses - Create a new course

PUT /api/admin/courses/{courseId} - Update a course

DELETE /api/admin/courses/{courseId} - Delete a course

POST /api/admin/courses/{courseId}/assign-instructor - Assign instructor to a course

GET /api/admin/courses/{courseId}/students - Get students in a course

GET /api/admin/courses/by-instructor?email={email} - Get courses by instructor

GET /api/admin/courses/{courseId}/enrollment-count - Get student count in a course

# Assignment Management

GET /api/admin/assignments - Retrieve all assignments

GET /api/admin/assignments/{assignmentId} - Retrieve assignment details

POST /api/admin/assignments - Create an assignment

PUT /api/admin/assignments/{assignmentId} - Update an assignment

DELETE /api/admin/assignments/{assignmentId} - Delete an assignment

GET /api/admin/assignments/due-before?date=YYYY-MM-DD - Retrieve assignments due before a date

# Student Endpoints

GET /api/students/{studentId} - Get student profile

PUT /api/students/{studentId} - Update student profile

GET /api/students/{studentId}/courses - Get enrolled courses

POST /api/students/{studentId}/courses/{courseId} - Enroll in a course

DELETE /api/students/{studentId}/courses/{courseId} - Withdraw from a course

GET /api/students/{studentId}/assignments - Get student assignments

# Authentication Endpoints

POST /api/auth/register - Register a new user

POST /api/auth/login - Authenticate user and obtain token

# Notes

Use Postman for testing API requests.

Implement proper security using Spring Security.
