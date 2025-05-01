# Airbnb Clone Project

The **Airbnb Clone Project** is a comprehensive, real-world application designed to simulate the development of a robust booking platform like Airbnb. This project emphasizes backend systems, database design, API development, and application security.

---

## Project Goals

- **User Management**: Implement secure user registration, login, and profile management.
- **Property Management**: Allow users to create, update, and retrieve property listings.
- **Booking System**: Enable users to book properties and manage their reservations.
- **Payment Processing**: Integrate a system to handle transactions and log payment details.
- **Review System**: Let users leave reviews and ratings for properties.
- **Data Optimization**: Ensure efficient database queries and storage through optimization.

---

## Team Roles

- **Backend Developer**: Develop API endpoints, business logic, and integrate external services.
- **Database Administrator**: Design and maintain the database schema, ensure performance, backups, and indexing.
- **DevOps Engineer**: Set up and manage infrastructure, Docker containers, CI/CD pipelines, and deployment automation.
- **QA Engineer**: Write test cases, perform manual and automated testing to ensure backend reliability and correctness.

---

## Technology Stack

- **Django**: A high-level Python web framework used to build the core backend and business logic.
- **Django REST Framework (DRF)**: A toolkit for building RESTful APIs quickly and flexibly.
- **PostgreSQL**: A robust relational database system to store and manage application data.
- **GraphQL**: A query language to provide efficient, flexible, and precise data retrieval for clients.
- **Celery**: Manages asynchronous tasks like email notifications or delayed operations.
- **Redis**: Used for caching and managing Celery queues and session data.
- **Docker**: Provides consistent development and production environments via containerization.
- **CI/CD Pipelines**: Automates testing, building, and deployment to improve code reliability and delivery speed.

---

## Database Design

### Key Entities and Fields:

1. **Users**
   - `id`
   - `name`
   - `email`
   - `password_hash`
   - `is_host`

2. **Properties**
   - `id`
   - `user_id` (foreign key to Users)
   - `title`
   - `description`
   - `location`

3. **Bookings**
   - `id`
   - `user_id` (foreign key to Users)
   - `property_id` (foreign key to Properties)
   - `start_date`
   - `end_date`

4. **Reviews**
   - `id`
   - `user_id`
   - `property_id`
   - `rating`
   - `comment`

5. **Payments**
   - `id`
   - `booking_id` (foreign key to Bookings)
   - `amount`
   - `status`
   - `transaction_date`

### Relationships:
- A **User** can create multiple **Properties**.
- A **Booking** is made by a **User** for a **Property**.
- A **Property** can have multiple **Reviews**.
- A **Payment** is linked to a specific **Booking**.

---
