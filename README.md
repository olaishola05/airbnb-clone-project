# airbnb-clone-project

## Brief Overview

The Airbnb Clone Project is a comprehensive, real-world application designed to simulate the development of a robust booking platform like Airbnb. It involves a deep dive into full-stack development, focusing on backend systems, database design, API development, and application security. This project enables learners to understand complex architectures, workflows, and collaborative team dynamics while building a scalable web application. To develop an understanding of integrating technologies like Django, MySQL, and GraphQL in a unified ecosystem.

## Team Roles

### Backend Developer

Responsible for implementing API endpoints, database schemas, and business logic.

### Database Administrator

Manages database design, indexing, and optimizations.

### DevOps Engineer

Handles deployment, monitoring, and scaling of the backend services.

### QA Engineer

Ensures the backend functionalities are thoroughly tested and meet quality standards.

## Technology Stack

- **Python**: The primary programming language used for backend development.
- **Django**: A high-level Python web framework used for building the RESTful API.
- **Django REST Framework**: Provides tools for creating and managing RESTful APIs.
- **PostgreSQL**: A powerful relational database used for data storage.
- **GraphQL**: Allows for flexible and efficient querying of data.
- **Celery**: For handling asynchronous tasks such as sending notifications or processing payments.
- **Redis**: Used for caching and session management.
- **Docker**: Containerization tool for consistent development and deployment environments.
- **CI/CD Pipelines**: Automated pipelines for testing and deploying code changes.

## Database Design

The database design for the Airbnb Clone Project is crucial for ensuring data integrity, scalability, and performance. The following key entities and their relationships are defined:

1. **User**: Represents the users of the platform, including hosts and guests.
   - Attributes: user_id, email, password, name, role (host/guest), etc.

2. **Property**: Represents the listings available for booking.
   - Attributes: property_id, host_id (FK), title, description, location, price, etc.
   - Relationships: Belongs to a User (host).

3. **Booking**: Represents a booking made by a guest for a specific property.
   - Attributes: booking_id, property_id (FK), guest_id (FK), start_date, end_date, status, etc.
   - Relationships: Belongs to a Property and a User (guest).

4. **Review**: Represents reviews left by guests for properties.
   - Attributes: review_id, property_id (FK), guest_id (FK), rating, comment, etc.
   - Relationships: Belongs to a Property and a User (guest).

5. **Payment**: Represents payment transactions for bookings.
   - Attributes: payment_id, booking_id (FK), amount, payment_method, status, etc.
   - Relationships: Belongs to a Booking.