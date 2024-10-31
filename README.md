# COM5003 - Spring Boot Application

# Student Management System

This is a basic Spring Boot application for managing students, built for learning and practice purposes. It demonstrates how to create a RESTful API using Spring Boot, Spring Data JPA, and H2 Database.

## Project Overview

The **Student Management System** allows users to:
- Add a new student
- View all students
- Retrieve details of a specific student
- Update a student's details
- Delete a student

## Technologies Used

- **Java 11**
- **Spring Boot 2.5**
- **Spring Data JPA**
- **H2 Database (in-memory)**

## Project Structure

src ├── main │ ├── java │ │ └── com.example.studentapp │ │ ├── StudentAppApplication.java # Main Application Class │ │ ├── controller │ │ │ └── StudentController.java # REST Controller │ │ ├── entity │ │ │ └── Student.java # Student Entity │ │ ├── repository │ │ │ └── StudentRepository.java # Repository Interface │ │ └── service │ │ └── StudentService.java # Service Layer │ └── resources │ ├── application.properties # Configuration │ └── data.sql # Optional, seed data for testing └── test # Unit and Integration Tests



## Getting Started

### Prerequisites

- **Java 11** or higher
- **Maven** (or use the built-in Maven wrapper)

### Installation

1. **Clone the repository**:
    ```bash
    git clone https://github.com/yourusername/student-management-system.git
    cd student-management-system
    ```

2. **Build the project**:
    ```bash
    mvn clean install
    ```

3. **Run the application**:
    ```bash
    mvn spring-boot:run
    ```

4. **Access the H2 Database Console** (optional):
   - Go to: `http://localhost:8080/h2-console`
   - JDBC URL: `jdbc:h2:mem:testdb`
   - Username: `sa`
   - Password: `password`

## Configuration

The `application.properties` file is configured to use H2 in-memory database by default. If you wish to use an external database, update the following properties in `application.properties`:

```properties
spring.datasource.url=jdbc:mysql://localhost:3306/yourdatabase
spring.datasource.username=yourusername
spring.datasource.password=yourpassword
spring.jpa.hibernate.ddl-auto=update
REST API Endpoints
Base URL: /api/students
HTTP Method	Endpoint	Description
GET	/api/students	Retrieve all students
GET	/api/students/{id}	Retrieve student by ID
POST	/api/students	Create a new student
PUT	/api/students/{id}	Update an existing student
DELETE	/api/students/{id}	Delete a student by ID
Example API Usage
Create a new student:

bash

curl -X POST -H "Content-Type: application/json" -d '{"firstName": "Alice", "lastName": "Johnson", "email": "alice.johnson@example.com"}' http://localhost:8080/api/students
Get all students:

bash

curl -X GET http://localhost:8080/api/students
Update a student:

bash

curl -X PUT -H "Content-Type: application/json" -d '{"firstName": "Alice", "lastName": "Smith", "email": "alice.smith@example.com"}' http://localhost:8080/api/students/1
Delete a student:

bash

curl -X DELETE http://localhost:8080/api/students/1
Testing
Run the following command to execute unit and integration tests:

bash

mvn test
License
This project is licensed under the MIT License - see the LICENSE file for details.

Happy Coding!

arduino


This file provides a clear overview and instructions for using the application, making it easier for others to get started.

2/2







