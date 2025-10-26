Employee Management REST API

Description:
A Spring Boot-based REST API for managing employee records. Supports CRUD operations with MySQL database integration. Designed for learning full-stack development and backend REST APIs.

Tech Stack

Backend: Java, Spring Boot

Database: MySQL

Testing: JUnit

Tools: Maven, Postman

Features

Create, Read, Update, Delete (CRUD) employee records

RESTful API design

MySQL database integration

Unit tests for service layer

Getting Started
Prerequisites

Java 17

Maven

MySQL

Setup

Clone the repository:

git clone https://github.com/YOUR_USERNAME/EmployeeManagement.git


Create MySQL database:

CREATE DATABASE employee_db;


Update src/main/resources/application.properties with your MySQL credentials:

spring.datasource.url=jdbc:mysql://localhost:3306/employee_db
spring.datasource.username=root
spring.datasource.password=YOUR_PASSWORD
spring.jpa.hibernate.ddl-auto=update


Build and run the application:

mvn clean install
mvn spring-boot:run


Test endpoints using Postman or cURL. Example:

GET http://localhost:8080/employees
POST http://localhost:8080/employees

Project Structure
src/
 ├─ main/java/com/example/employeemanagement
 │    ├─ controller/EmployeeController.java
 │    ├─ service/EmployeeService.java
 │    ├─ model/Employee.java
 │    └─ repository/EmployeeRepository.java
 └─ resources/application.properties

Testing

Unit tests are in src/test/java/com/example/employeemanagement/service/EmployeeServiceTest.java.

Run tests with:

mvn test
