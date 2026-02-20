# Ticketing Project - Jira Clone

A robust ticketing system inspired by Jira, built with Spring Boot. This application enables teams to track projects, tasks, and user assignments efficiently.

## 🚀 Features

- **User Management** - Create and manage users with different roles
- **Project Management** - Create and track multiple projects
- **Task Tracking** - Create, assign, and track tasks with various statuses
- **Role-Based Access Control** - Different permissions for different user types
- **RESTful API** - Well-designed endpoints for all operations
- **Exception Handling** - Comprehensive error handling throughout the application
- **DTO Layer** - Clean separation between entity and API models
- **Mapping** - Efficient object mapping between layers

## 🏗️ Technology Stack

- **Framework**: Spring Boot
- **Security**: Keycloak Integration
- **Database**: JPA / Hibernate
- **Build Tool**: Maven/Gradle
- **API Style**: REST
- **Architecture**: Multi-layered (Controller-Service-Repository)


## 📁 Project Structure

src/

├── main/

│ └── java/

│ └── com/yourpackage/

│ ├── annotation/ # Custom annotations

│ ├── aspect/ # AOP aspects for cross-cutting concerns

│ ├── config/ # Configuration classes

│ ├── controller/ # REST endpoints

│ │ ├── ProjectController.java

│ │ ├── TaskController.java

│ │ └── UserController.java

│ ├── dto/ # Data Transfer Objects

│ ├── entity/ # JPA entities

│ ├── enums/ # Enum definitions

│ ├── exception/ # Custom exceptions and handlers

│ ├── mapper/ # Entity-DTO mappers

│ ├── repository/ # Data access layer

│ ├── service/ # Business logic layer

│ └── TicketingProjectRestApplication.java


## 🔧 API Endpoints

### User Controller
- `GET /api/users` - Get all users
- `GET /api/users/{id}` - Get user by ID
- `POST /api/users` - Create new user
- `PUT /api/users/{id}` - Update user
- `DELETE /api/users/{id}` - Delete user

### Project Controller
- `GET /api/projects` - Get all projects
- `GET /api/projects/{id}` - Get project by ID
- `POST /api/projects` - Create new project
- `PUT /api/projects/{id}` - Update project
- `DELETE /api/projects/{id}` - Delete project
- `GET /api/projects/{id}/tasks` - Get all tasks for a project

### Task Controller
- `GET /api/tasks` - Get all tasks
- `GET /api/tasks/{id}` - Get task by ID
- `POST /api/tasks` - Create new task
- `PUT /api/tasks/{id}` - Update task
- `DELETE /api/tasks/{id}` - Delete task
- `PATCH /api/tasks/{id}/assign` - Assign task to user
- `PATCH /api/tasks/{id}/status` - Update task status

## 🛡️ Security

The application uses **Keycloak** for:
- Authentication and authorization
- Single Sign-On (SSO) capability
- User federation
- Social login support
- Centralized security management

## 🎯 Key Components

### Entities
- **User** - System users with roles and permissions
- **Project** - Projects containing multiple tasks
- **Task** - Individual work items with status, priority, and assignments

### Enums
- Task Status (TODO, IN_PROGRESS, REVIEW, DONE)
- Task Priority (LOW, MEDIUM, HIGH, CRITICAL)
- User Roles (ADMIN, PROJECT_LEAD, DEVELOPER, REVIEWER)

### Exception Handling
- Custom exception classes for different error scenarios
- Global exception handler for consistent error responses
- Validation error handling

## 🚀 Getting Started

### Prerequisites
- Java 11 or higher
- Maven or Gradle
- Keycloak server (for authentication)
- PostgreSQL/MySQL (or your preferred database)

### Installation

1. Clone the repository
```bash
git clone https://github.com/yourusername/ticketing-project.git


    Configure Keycloak

        Set up Keycloak server

        Configure realm and clients

        Update application.yml with Keycloak settings

    Configure database

        Update database credentials in application.yml

    Run the application

📝 Configuration

Key configuration files:

    application.yml - Main application configuration

    keycloak.json - Keycloak specific configuration

    pom.xml/build.gradle - Dependencies

🧪 Testing

The project includes comprehensive tests:

    Unit tests for services

    Integration tests for controllers

    Repository tests with test database
