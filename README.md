# University_Course_Management_System

## Overview

This is a Spring Boot-based University Course Management System that allows admins, instructors, and students to manage courses, assignments, and enrollments efficiently.

## Technologies Used

    -Java (Spring Boot)
    
    -Spring Web
    
    -Spring Data JPA
    
    -Spring DevTools
    
    -MySQL Database

## Installation & Setup

1.Clone the repository:

    git clone <repository_url>
    
    Open the project in Eclipse as a Spring Starter Project.

2.Ensure you have the following dependencies installed:

    -Spring Web
    
    -Spring Data JPA
    
    -Spring DevTools
    
    -MySQL Connector

3.Configure your database in application.properties:

    spring.datasource.url=jdbc:mysql://localhost:3306/university_db
    spring.datasource.username=root
    spring.datasource.password=yourpassword
    spring.jpa.hibernate.ddl-auto=update

4. Run the application from UniversityApplication.java/ as a spring boot application.

# API Endpoints

## Admin Endpoints

## Student Management

    -GET /api/admin/students - Retrieve all students
    
    -GET /api/admin/students/{studentId} - Get student details
    
    -POST /api/admin/students - Create a new student
    
    -PUT /api/admin/students/{studentId} - Update student details
    
    -DELETE /api/admin/students/{studentId} - Delete a student

## Instructor Management

    -GET /api/admin/instructors - Retrieve all instructors
    
    -GET /api/admin/instructors/{instructorId} - Get instructor details
    
    -POST /api/admin/instructors - Create a new instructor
    
    -PUT /api/admin/instructors/{instructorId} - Update instructor details
    
    -DELETE /api/admin/instructors/{instructorId} - Delete an instructor

## Course Management

    -GET /api/admin/courses - Retrieve all courses
    
    -GET /api/admin/courses/{courseId} - Get course details
    
    -POST /api/admin/courses - Create a new course
    
    -PUT /api/admin/courses/{courseId} - Update course details
    
    -DELETE /api/admin/courses/{courseId} - Delete a course
    
    -POST /api/admin/courses/{courseId}/assign-instructor - Assign an instructor to a course
    
    -GET /api/admin/courses/{courseId}/students - Get enrolled students
    
    -GET /api/admin/courses/by-instructor?email={email} - Get courses by instructor
    
    -GET /api/admin/courses/{courseId}/enrollment-count - Get enrollment count

## Assignment Management

    -GET /api/admin/assignments - Retrieve all assignments
    
    -GET /api/admin/assignments/{assignmentId} - Get assignment details
    
    -POST /api/admin/assignments - Create a new assignment
    
    -PUT /api/admin/assignments/{assignmentId} - Update an assignment
    
    -DELETE /api/admin/assignments/{assignmentId} - Delete an assignment
    
    -GET /api/admin/assignments/due-before?date=YYYY-MM-DD - Get assignments due before a date

## Student Endpoints

    -GET /api/students/{studentId} - Get student profile
    
    -PUT /api/students/{studentId} - Update student profile
    
    -GET /api/students/{studentId}/courses - Get enrolled courses
    
    -POST /api/students/{studentId}/courses/{courseId} - Enroll in a course
    
    -DELETE /api/students/{studentId}/courses/{courseId} - Withdraw from a course
    
    -GET /api/students/{studentId}/assignments - Get assignments

## Authentication Endpoints

    -POST /api/auth/register - Register a new user
    
    -POST /api/auth/login - Authenticate user and get a token

## Notes

Use Postman for testing API requests.

Implement proper security using Spring Security.
