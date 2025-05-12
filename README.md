# Airbnb Clone Project

## Overview

The Airbnb Clone Project is a backend-focused clone of the Airbnb platform. The aim is to simulate building a scalable real-world web application with user and property management, booking functionality, payment systems, and reviews. This project helps learners master backend development, database design, API security, CI/CD practices, and GitHub workflows.

### Project Goals

- Build a scalable, secure backend system.
- Practice full-cycle software engineering with documentation and automation.
- Apply team collaboration principles and CI/CD integration.

## Team Roles

| Role | Responsibility |
|------|----------------|
| Backend Developer | Implements APIs, integrates the database, and ensures correct business logic. |
| Database Administrator | Designs, manages, and optimizes the database schema for performance and scalability. |
| DevOps Engineer | Sets up CI/CD pipelines, manages deployment automation, and ensures smooth delivery. |
| QA Engineer | Designs test cases, performs manual and automated testing to ensure the system works as intended. |
| Project Manager | Oversees the workflow, tracks task progress, and ensures collaboration across the team. |

## Technology Stack

| Technology | Purpose |
|------------|---------|
| **Django** | A powerful Python web framework used to build the RESTful APIs and handle backend logic. |
| **PostgreSQL** | A robust, open-source relational database system used for storing user, property, booking, and payment data. |
| **GraphQL** | An alternative API query language to allow efficient fetching of nested resources. |
| **Docker** | Used for containerizing the application and creating reproducible development environments. |
| **GitHub Actions** | Automates tasks such as testing, linting, and deployment through CI/CD pipelines. |

## Database Design

The application database is structured around the following key entities:

### Users

- `id` (Primary Key)
- `name`
- `email`
- `password_hash`
- `role` (host or guest)

### Properties

- `id` (Primary Key)
- `title`
- `description`
- `location`
- `price_per_night`
- `host_id` (Foreign Key to Users)

### Bookings

- `id` (Primary Key)
- `property_id` (Foreign Key to Properties)
- `user_id` (Foreign Key to Users)
- `start_date`
- `end_date`

### Reviews

- `id` (Primary Key)
- `user_id` (Foreign Key to Users)
- `property_id` (Foreign Key to Properties)
- `rating`
- `comment`

### Payments

- `id` (Primary Key)
- `booking_id` (Foreign Key to Bookings)
- `amount`
- `status`
- `payment_method`

#### Relationships

- A **User** can book many **Properties**.
- A **Property** can have many **Bookings** and **Reviews**.
- A **Booking** has one **Payment**.
- A **User** can leave multiple **Reviews**.

## Feature Breakdown

### User Management

Handles user registration, login, profile management, and authentication. Users can be either hosts (list properties) or guests (book properties).

### Property Management

Hosts can create, update, or delete property listings with details like photos, pricing, and descriptions.

### Booking System

Enables guests to search for properties and book available dates, with automatic conflict resolution for booking dates.

### Review System

Allows guests to leave reviews for properties they have booked, contributing to the property's overall rating.

### Payment Integration

Handles secure processing of bookings via payment gateways and tracks transaction history for users.

## API Security

Security is a major priority for protecting user data and ensuring trusted transactions. Key measures include:

- **Authentication:** Use of JWT or token-based authentication for user sessions.
- **Authorization:** Role-based access to resources (e.g., only hosts can modify properties).
- **Rate Limiting:** Protects APIs from abuse and brute-force attacks.
- **Input Validation:** Prevents injection attacks and data corruption.
- **HTTPS Enforcement:** Ensures secure communication.

### Why It Matters

- **Protecting User Data:** Prevents identity theft and unauthorized access.
- **Securing Payments:** Ensures transactions can't be intercepted or altered.
- **Regulatory Compliance:** Adheres to data protection laws and policies.

## CI/CD Pipeline

### What is CI/CD?

CI/CD (Continuous Integration/Continuous Deployment) automates the process of testing, building, and deploying code. It increases development efficiency and reduces human errors during deployment.

### Tools Used

- **GitHub Actions:** Automates tests and deploys code to staging or production environments.
- **Docker:** Ensures that development and production environments are consistent.

### Pipeline Overview

1. On every push, code is linted and tested.
2. If tests pass, the build is packaged into a Docker container.
3. The image is pushed to a container registry.
4. Deployment is triggered to a cloud platform or server.

---

> ✅ All tasks completed and documented in this README.md.  
> 📌 GitHub Repository: [airbnb-clone-project](https://github.com/OlukaGibson/airbnb-clone-project)

