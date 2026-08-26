# Student Management System

A RESTful Student Management System built using Spring Boot, Spring Data JPA, and MySQL.

## Technologies Used

- Java 17
- Spring Boot
- Spring Data JPA
- MySQL
- Maven
- REST API

## Project Features

- Add a new student
- Get all students
- Get a student by ID
- Delete a student by ID
- MySQL database integration

## API Endpoints

### 1. Add Student

**POST** `/students`

Request Body:

```json
{
  "name": "Rahul",
  "email": "rahul@gmail.com",
  "course": "CSE"
}
