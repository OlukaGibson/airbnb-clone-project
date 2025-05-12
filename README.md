# Airbnb Clone Project

## Project Overview
This is a backend-focused clone of Airbnb, designed to replicate core functionalities such as user registration, property listings, and booking systems. The project emphasizes backend development practices, including API security, CI/CD integration, and database design.

## Tech Stack
- Django
- PostgreSQL
- GraphQL
- Docker
- GitHub Actions


## Team Roles

- **Backend Developer**: Builds and maintains APIs, handles business logic, and integrates database models.
- **Database Administrator**: Designs, optimizes, and secures the database structure.
- **DevOps Engineer**: Manages CI/CD pipelines, Docker containers, and deployment processes.
- **Project Manager**: Oversees project timelines and task allocations.


## Technology Stack

- **Django**: Web framework for creating RESTful APIs.
- **PostgreSQL**: Relational database for storing structured data.
- **GraphQL**: Query language for efficient data retrieval.
- **Docker**: Containerization tool to create reproducible development environments.
- **GitHub Actions**: CI/CD tool for automating builds and deployments.


## Database Design

### Entities:
- **User**: `id`, `email`, `password`, `name`, `is_host`
- **Property**: `id`, `user_id`, `title`, `description`, `price`
- **Booking**: `id`, `user_id`, `property_id`, `start_date`, `end_date`
- **Review**: `id`, `booking_id`, `rating`, `comment`
- **Payment**: `id`, `booking_id`, `amount`, `payment_status`

### Relationships:
- A **User** can list multiple **Properties**
- A **Booking** is made by a **User** for a **Property**
- A **Review** is tied to a **Booking**
- A **Payment** is linked to a **Booking**


## Feature Breakdown

- **User Management**: Registration, login, and role (host/guest) management.
- **Property Listings**: Hosts can add, update, and delete properties.
- **Booking System**: Guests can book available properties with date validation.
- **Review System**: Users can leave reviews after stays.
- **Payment Integration**: Secure handling of booking payments.


## API Security

- **Authentication**: Using JWT tokens for secure user sessions.
- **Authorization**: Role-based access control to restrict actions.
- **Rate Limiting**: Prevents abuse by limiting API calls per user/IP.
- **Input Validation**: Prevents injection attacks and malformed data.
- **HTTPS**: Encrypts communication between client and server.

Security is crucial for protecting sensitive data like personal info and payments.


## CI/CD Pipeline

CI/CD (Continuous Integration / Continuous Deployment) automates testing and deployment.

### Tools:
- **GitHub Actions**: Runs tests and deploys code on push.
- **Docker**: Ensures consistent dev/test/prod environments.
- **Heroku / Render / Railway**: Platforms to host the app.

This improves reliability and reduces manual deployment errors.
