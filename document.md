# 11-Java-Employee-Payroll-System

->Welcome to the Employee Payroll System documentation. This guide provides comprehensive information on the project's structure, configuration, components, and usage.

->Table of Contents

1. [Introduction](#introduction)
2. [Project Structure](#project-structure)
3. [Database Configuration](#database-configuration)
4. [Spring Boot Backend](#spring-boot-backend)
5. [JSP Views](#jsp-views)
6. [Tomcat Configuration](#tomcat-configuration)
7. [Security Measures](#security-measures)
8. [Error Handling](#error-handling)
9. [API Documentation](#api-documentation)
10. [User Guide](#user-guide)

### Introduction

->The Employee Payroll System is a Java-based application designed to manage employee data, calculate salaries, and process payroll efficiently. This documentation outlines the system's architecture, components, and usage instructions.

### Project Structure

->The project follows a modular structure:

-> **src/main/java**: Contains Java source code.
  -> `com.inf.controller`: Controllers for handling web requests.
  -> `com.inf.entity`: Entity classes representing database entities.
  -> `com.inf.exception`: Custom exceptions.
  -> `com.inf.repository`: Spring Data JPA repositories.
  -> `com.inf.service`: Service classes for business logic.
-> **src/main/resources**: Configuration files and JSP views.
-> **src/main/webapp/WEB-INF/pages**: JSP view templates.
-> **pom.xml**: Maven project configuration.

### Database Configuration

-> The application uses an Oracle Database. Configure the database connection in `application.properties`:
-> properties:-
spring.datasource.driver-class-name=oracle.jdbc.driver.OracleDriver
spring.datasource.url=jdbc:oracle:thin:@localhost:1521:orcl
spring.datasource.username=mohitdb
spring.datasource.password=mohitdb

### Spring Boot Backend
->The backend is developed using Spring Boot:

->Controllers (EmployeeOperationsController): Handle HTTP requests.
->Services (EmployeeMgmtServiceImpl): Contain business logic.
->Repositories (IEmployeeRepo): Spring Data JPA repositories for database interaction.
->Exception Handling: Custom exception classes (EmployeeNotFoundException) for specific error scenarios.
### JSP Views
->JSP views are used for the user interface. View templates are located in src/main/webapp/WEB-INF/pages.

->register_emp.jsp: Form for registering a new employee.
->show_emp_report.jsp: Display all employee data in a tabular format.
->show_home.jsp: Home page with navigation links.
->update_emp.jsp: Update / Edit page.

### Tomcat Configuration
->The application uses Tomcat as the embedded servlet container. Configuration details are specified in application.properties and dependencies in the pom.xml file.

### Security Measures
->Security measures include data validation, exception handling, and access controls. Further enhancements can be added based on specific project requirements.

### Error Handling
->The application implements error handling for scenarios such as invalid employee IDs (EmployeeNotFoundException). Exception messages provide informative error details.

### API Documentation
->The application follows a monolithic architecture with a user interface built using JSP views. As such, there are no separate API endpoints.

### User Guide
#### Installation
->Clone the repository.
->Set up the Oracle Database and configure application.properties.
->Build the project using Maven: mvn clean install.
->Run the Spring Boot application: mvn spring-boot:run.

#### Configuration
->Database configuration: Update application.properties for any database-related changes.

#### User Interface (JSP Views)
-> Register New Employee: Access the registration form at /emp_add.
-> Employee Report: View all employee data at /emp_report.
-> Edit / Update Data: Edit / Update all employee data at /update_emp.

#### Functionality
->Adding a New Employee: Fill in the registration form with employee details and submit.
->Viewing Employee Report: Access the employee report to see a tabular display of all employees.

#### Database Interaction
->The application automatically updates the database based on user actions.

#### Troubleshooting
->Database Connection Issues: Verify the database configuration in application.properties.
->Application Errors: Refer to error messages for guidance.




