## Social Media Backend API

A robust backend service for social media applications. Built using Spring Boot, Spring Security, and Hibernate.
Implements secure token authentication, post interaction APIs, and advanced data analytics endpoints.

A production-grade, highly scalable Social Media Backend Service built using Java 17 and Spring Boot 3.x.
This API manages core social media operations, focusing on microservice-ready design patterns, stateless security, 
and optimized relational data mapping.

##  Key Features

1. Stateless JWT Authentication: Secure user signup and login flow utilizing Spring Security and JSON Web Tokens (JWT).

2. Post Interactions (CRUD): Complete control over creating, reading, updating, and deleting posts, along with full
    like and save functionalities.

3. Automated Story Expiry: Advanced backend logic automatically handles a 24-hour expiration window for user stories.

4. Smart Feed & Filtering: Optimized database queries to deliver user feeds sorted by activity, recency, or specific filters.

5. Analytics Endpoint: Specialized metrics and insights generation for user engagement data.

6. Role-Based Access Control (RBAC): Tiered endpoint protection to ensure proper data privacy and authorization.

## Tech Stack

- **Language:** Java 17
- **Framework:** Spring Boot 3.x (Spring Security, Spring Data JPA)
- **Database:** MySQL 8.0
- **Token Security:** JJWT (Java JWT Library)
- **Build Tool:** Maven
- **Testing & API Documentation:** Postman

##  System Architecture

```text
├── .mvn/                  # Maven wrapper configuration
├── src/
│   └── main/
│       ├── java/          # Core Java source code (Controllers, Services, Models, Security)
│       └── resources/     # Application properties and SQL configuration files
├── .gitignore             # Git ignore configurations
├── pom.xml                # Maven project dependencies
└── README.md
