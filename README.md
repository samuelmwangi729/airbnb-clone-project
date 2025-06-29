# AirBnB Clone – Full Stack Web Application

## Project Overview

This project is a full-stack web application that replicates the core functionalities of AirBnB, a popular platform for listing and booking accommodations. Users can browse listings, view detailed property information, and make secure bookings. The application is built using modern technologies with a focus on usability, performance, security, and real-world development practices.

---

## Project Goals

- Replicate core features of AirBnB in a scalable web application
- Implement both frontend and backend using best practices
- Ensure a responsive and accessible design
- Practice clean architecture and collaborative development
- Deploy using cloud services and containerization
- Integrate CI/CD for efficient development lifecycle

---

## Technology Stack

This section outlines the technologies used in the project and their roles.

- **Django**: Backend web framework for handling routing, business logic, and API creation.
- **MySQL**: Relational database for storing structured data such as users, bookings, and listings.
- **GraphQL**: API query language to optimize frontend data fetching by requesting only needed fields.
- **React**: JavaScript library for building the user interface and managing client-side state.
- **Docker**: Containerization tool for creating consistent environments during development and deployment.
- **GitHub Actions**: CI/CD tool used to automate testing and deployment workflows.
- **Markdown**: Used for writing project documentation such as this `README.md` file.

> These technologies collectively support modular design, fast development, and reliable deployment of the platform.

---

## Database Design

This section describes the entities used in the application, their fields, and relationships.

### Key Entities and Fields

#### Users
- `user_id`: Unique identifier for each user
- `name`: Full name of the user
- `email`: User’s unique email address
- `password_hash`: Secure hashed password
- `role`: User role (guest, host, admin)

#### Properties
- `property_id`: Unique ID of the property
- `owner_id`: Reference to the User (host)
- `title`: Title of the property listing
- `description`: Detailed description of the property
- `location`: Geographical location

#### Bookings
- `booking_id`: Unique ID for each booking
- `user_id`: ID of the guest making the booking
- `property_id`: ID of the booked property
- `start_date`: Booking start date
- `end_date`: Booking end date

#### Reviews
- `review_id`: Unique review identifier
- `booking_id`: Booking associated with the review
- `rating`: Numeric rating (1–5)
- `comment`: Text feedback
- `created_at`: Timestamp of review

#### Payments
- `payment_id`: Unique payment transaction ID
- `booking_id`: Associated booking
- `amount`: Payment amount
- `payment_method`: Method (e.g., card, PayPal)
- `payment_status`: Status (e.g., completed)

### Entity Relationships

- One **User** (host) can own many **Properties**
- One **User** (guest) can make many **Bookings**
- One **Property** can have many **Bookings**
- One **Booking** can have one **Review** and one **Payment**

> This well-structured relational model ensures all entities interact in a scalable, maintainable way.

---

## Feature Breakdown

### User Management
- User registration, login, and role-based access control

### Property Management
- Hosts can list and manage properties with images and descriptions

### Booking System
- Guests can book properties for specific dates and avoid double-bookings

### Reviews and Ratings
- Guests can leave feedback on completed bookings

### Payment Processing
- Supports secure payments and tracks transaction statuses

### Authentication and Authorization
- JWT-based session management with protected routes

### Responsive UI/UX
- Designed mobile-first and compliant with accessibility standards

> Each feature was implemented to reflect real-world booking systems.

---

## API Security

### Key Security Measures

- **Authentication**: JWT used to authenticate users and sessions
- **Authorization**: Role-based access to APIs based on user type
- **Rate Limiting**: Prevent brute-force and abuse using request throttling
- **Encryption**: HTTPS and password hashing to secure data in transit and at rest
- **Input Validation**: Prevents SQL injection, XSS, and other attacks
- **Secure Payments**: PCI-DSS-compliant payment providers ensure financial security

> Security features protect user data, uphold integrity, and maintain trust.

---

## CI/CD Pipeline

### What is CI/CD?

CI/CD stands for Continuous Integration and Continuous Deployment. It's a DevOps practice that automates code testing and delivery processes, allowing teams to:

- Detect and fix bugs early
- Ship features faster
- Maintain code quality and reliability

### Tools Used

- **GitHub Actions**: Runs automated tests and deploys code upon pull requests or merges
- **Docker**: Packages the app into containers for consistency across dev and production

> CI/CD enhances efficiency, reduces manual errors, and supports rapid development workflows.

---

## Team Roles

Each member has a clear role and responsibility that reflects a real-world software development team.

### Backend Developer

Builds the server, APIs, and implements core business logic in Django. Ensures backend reliability and performance.

### Database Administrator (DBA)

Designs the database schema, manages indexes, runs backups, and ensures data consistency and query optimization.

### Frontend Developer

Builds and maintains the client interface using React. Ensures responsive, accessible, and attractive UI.

### DevOps Engineer

Implements Docker containers and GitHub Actions for automation. Manages environments and system uptime.

### QA Engineer / Tester

Writes and automates test cases, runs regression tests, and ensures the application meets quality standards.

### Product Owner

Acts as liaison between stakeholders and developers. Prioritizes features and ensures business value is delivered.

### Project Manager

Coordinates the team, sets milestones, and manages agile ceremonies. Tracks progress and resolves blockers.

### UX/UI Designer

Uses Figma to design interfaces and user flows. Ensures visual clarity and excellent user experience.

> A clear division of labor helps ensure project success through effective collaboration.
