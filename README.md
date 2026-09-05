# MediSlot - Smart Doctor Appointment Booking System

MediSlot is a Java Spring Boot web application for booking appointments with verified doctors. The system provides separate workflows for patients, doctors, and administrators, ensuring secure and reliable appointment management.

## Features

### Patient Module

* Register and login
* Search verified doctors by specialization and city
* View available doctor slots
* Book appointments
* Cancel appointments
* View appointment history
* Submit reviews after completed appointments
* View notifications

### Doctor Module

* Register with professional details
* Wait for admin verification
* Login only after approval
* Generate appointment slots
* Manage appointment requests
* Approve or reject bookings
* Mark appointments as completed
* View notifications

### Admin Module

* Verify doctor applications
* Approve, reject, or suspend doctors
* Manage users
* Manage specializations
* View dashboard statistics
* Monitor appointments

## Tech Stack

* Java 17
* Spring Boot
* Spring Data JPA / Hibernate
* MySQL
* Thymeleaf
* HTML, CSS
* Maven
* BCrypt Password Encryption

## Doctor Verification Workflow

```text
Doctor Registration
        ↓
Admin Verification
        ↓
Approved / Rejected
        ↓
Doctor Login Access
```

Only approved doctors can create slots and receive appointments.

## Appointment Workflow

```text
Patient Books Slot
        ↓
PENDING
        ↓
Doctor Approves
        ↓
APPROVED
        ↓
Doctor Completes
        ↓
COMPLETED
        ↓
Patient Reviews
```

## Database Tables

| Table            | Purpose              |
| ---------------- | -------------------- |
| users            | Login accounts       |
| doctor_profiles  | Doctor information   |
| patient_profiles | Patient information  |
| specializations  | Medical specialties  |
| time_slots       | Appointment slots    |
| appointments     | Booking records      |
| reviews          | Patient reviews      |
| notifications    | System notifications |

## Project Structure

```text
medislot-smart-booking
├── pom.xml
├── README.md
└── src
    └── main
        ├── java
        │   └── com.medislot.app
        │       ├── config
        │       ├── controller
        │       ├── entity
        │       ├── repository
        │       └── service
        └── resources
            ├── application.properties
            ├── static
            ├── templates
            └── sql
```

## Prerequisites

* Java 17 or higher
* MySQL Server
* Maven
* IntelliJ IDEA / Eclipse / STS

## Database Setup

Create a database:

```sql
CREATE DATABASE medislot_db;
```

Update `application.properties`:

```properties
spring.datasource.url=jdbc:mysql://localhost:3306/medislot_db
spring.datasource.username=root
spring.datasource.password=YOUR_PASSWORD
```

## Run the Project

### Using IDE

1. Open the project.
2. Configure database credentials.
3. Run `MediSlotApplication.java`.
4. Open:

```text
http://localhost:8080
```

### Using Terminal

```bash
mvn spring-boot:run
```

Then open:

```text
http://localhost:8080
```

## Security Features

* BCrypt password hashing
* Session-based authentication
* Doctor approval before login
* User account management
* Double-booking prevention

## Future Enhancements

* Spring Security integration
* Email OTP verification
* Doctor document uploads
* Online payment gateway
* PDF prescriptions
* Reports and analytics
* Mobile app REST APIs

## Project Highlights

* Multi-role authentication
* Doctor verification workflow
* Appointment booking and management
* Patient reviews and notifications
* Secure database integration
* Real-world healthcare booking process

## Author

**Ankitha M**

Computer Science and Engineering Graduate

Java | Spring Boot | Hibernate | MySQL | Full Stack Development
