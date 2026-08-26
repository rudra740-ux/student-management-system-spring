# Student Management System

A RESTful Student Management System developed using Spring Boot, Spring Data JPA, and MySQL.

## Developed By

**Rudra Pratap Singh**

## Technologies Used

* Java 17
* Spring Boot
* Spring Data JPA
* MySQL
* Maven
* REST API
* Docker

## Project Features

* Add a new student
* Get all students
* Get a student by ID
* Delete a student by ID
* MySQL database integration

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
```

### 2. Get All Students

**GET** `/students`

Returns all students stored in the database.

### 3. Get Student by ID

**GET** `/students/{id}`

Example:

`/students/2`

Returns the student having the specified ID.

### 4. Delete Student

**DELETE** `/students/{id}`

Example:

`/students/2`

Deletes the student having the specified ID.

## Database

The project uses MySQL with Docker.

**Database Name:** `student_db`
**Username:** `root`
**Password:** `root`

## How to Run the Project

### First-Time Setup

Make sure Docker is running and the MySQL container has been created.

Start the existing MySQL container:

```bash
docker start student-mysql
```

Check that MySQL is running:

```bash
docker exec student-mysql mysqladmin ping -uroot -proot
```

Expected output:

```text
mysqld is alive
```

Then start the Spring Boot application:

```bash
./mvnw spring-boot:run
```

Wait until:

```text
Started StudentmanagementApplication
```

The application runs on:

`http://localhost:8080`

### After System or Codespace Restart

If the system or Codespace is shut down, the project code and database do **not** need to be created again.

After reopening the Codespace:

1. Check whether the MySQL container is running:

```bash
docker ps
```

2. If `student-mysql` is not running, start the existing container:

```bash
docker start student-mysql
```

3. Check MySQL:

```bash
docker exec student-mysql mysqladmin ping -uroot -proot
```

Expected output:

```text
mysqld is alive
```

4. Start Spring Boot:

```bash
./mvnw spring-boot:run
```

5. Wait for:

```text
Started StudentmanagementApplication
```

6. Keep the Spring Boot terminal running.

7. Open a new terminal to test the APIs.

**Important:** Do not create the database or MySQL container again if they already exist. Only restart the existing MySQL container and Spring Boot application.

## API Testing

The APIs can be tested using Postman.

Example:

```bash
curl http://localhost:8080/students
```

## API Flow

Postman sends an HTTP request to the Spring Boot REST Controller.

The Controller communicates with the Service layer.

The Service layer uses the Repository layer.

The Repository communicates with the MySQL database using Spring Data JPA.

## Project Structure

```text
src
└── main
    ├── java
    │   └── com.example.studentmanagement
    │       ├── controller
    │       ├── service
    │       ├── repository
    │       └── entity
    └── resources
        └── application.properties
```

## Developed By

**Rudra Pratap Singh**