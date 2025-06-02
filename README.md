
Contact Manager App

This project is a web application for managing contacts, built with an Angular frontend, a Spring Boot backend, and a PostgreSQL database.

Main Features:
- Create, edit, and deactivate contacts (soft delete)
- Display only active contacts
- Address data is stored as an embedded component in the database
- RESTful API using Spring Boot
- Reactive forms and routing in Angular
- Bootstrap for responsive styling

Technologies Used:
- Frontend: Angular 16, TypeScript
- Backend: Spring Boot 3, Java 17+
- Database: PostgreSQL
- Styling: Bootstrap 5
- Build tool: Maven

Project Structure Overview:
contactapp/
  contactapp-backend/
    - controller/: REST endpoints
    - service/: Business logic
    - repository/: JPA repositories for DB access
    - model/: Contact and Address entity classes

  contactapp-frontend/
    - components/: Angular components (form, list, edit, welcome)
    - app.routes.ts: Application routing

PostgreSQL Connection:
Database connection settings are defined in `application.properties`:
spring.datasource.url=jdbc:postgresql://localhost:5432/contactdb
spring.datasource.username=your_username
spring.datasource.password=your_password
spring.jpa.hibernate.ddl-auto=update

How to Run:

Backend:
cd contactapp-backend
./mvnw spring-boot:run

Frontend:
cd contactapp-frontend
npm install
ng serve

The frontend will run on http://localhost:4200  
The backend API is available at http://localhost:8080/contacts

Notes:
- Contacts are not physically deleted from the database; instead, they are marked inactive using an `active` flag.
- This application is fully local and suitable as a training or personal project.

Author:
Created by Georg Loibnegger as a learning project using Angular and Spring Boot.
