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

    ├── .mvn/                  # Maven wrapper configuration
    ├── src/
    │   └── main/
    │       ├── java/          # Core Java source code (Controllers, Services, Models, Security)
    │       └── resources/     # Application properties and SQL configuration files
    ├── .gitignore             # Git ignore configurations
    ├── pom.xml                # Maven project dependencies
    └── README.md

## Prerequisites

1. Java Development Kit (JDK) 17 installed

2. MySQL Server running locally

3.Maven installed (or use the provided ./mvnw wrapper)

Step 1: Clone the Repository

    git clone [https://github.com/sunidhimishra17/social-media-backend-api.git]
    
    cd social-media-backend-api
    
Step 2: Configure Database Settings

Open src/main/resources/application.properties (or application.yml) and update the MySQL configuration with your local database credentials:

    spring.datasource.url=jdbc:mysql://localhost:3306/YOUR_DB_NAME
    
    spring.datasource.username=YOUR_MYSQL_USERNAME
    
    spring.datasource.password=YOUR_MYSQL_PASSWORD
    
    spring.jpa.hibernate.ddl-auto=update
    
Step 3: Build and Run the Application

Using the terminal, compile and run the Spring Boot app:

On Windows:

    mvnw.cmd spring-boot:run

On macOS/Linux:

    chmod +x mvnw
    
    ./mvnw spring-boot:run
    
## Core API Endpoints

| HTTP Method | Endpoint| Description | Auth Required |
|:--- | :--- | :--- | :---|
|**POST**|'/api/auth/signup'|Register a new user profile|No|
|**POST**|'/api/auth/login'|Authenticate user & generate JWT token|No|
|**GET**|'/api/posts'|Retrieve optimized social media feed|Yes (JWT)|
|**POST**|'/api/posts'|Publish a new post|Yes (JWT)|
|**POST**|'/api/posts/{id}/like'|Toggle like status on a post|Yes (JWT)|
|**POST**|'/api/stories'|Upload a story (auto-expires in 24h)|Yes (JWT)|
|**GET**|'/api/analytics'|Fetch engagement insights dashboard|Yes (Admin)|
