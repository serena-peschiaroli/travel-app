# Travel App

This repository contains both the backend and frontend components of the **Travel App**, a web-based application designed to manage trips, stops, expenses, and categories for travelers.

## Table of Contents

- [Backend](#backend)
  - [Tech Stack](#tech-stack)
  - [Architecture](#architecture)
  - [API Endpoints](#api-endpoints)
  - [Future Improvements (Backend)](#future-improvements-backend)
- [Frontend](#frontend)
  - [Tech Stack (Frontend)](#tech-stack-frontend)
  - [Current Features](#current-features)
  - [Ongoing Work](#ongoing-work)
  - [Future Improvements (Frontend)](#future-improvements-frontend)
- [Contributing](#contributing)
- [License](#license)

## Backend

The backend is built with **Spring Boot** and follows a **RESTful API** design pattern to handle CRUD operations, business logic, and data persistence.

### Tech Stack

- **Java 17**: Core language for backend development.
- **Spring Boot 3**: Framework for building microservices and RESTful APIs.
- **Spring Data JPA**: For data persistence and ORM.
- **Hibernate**: ORM framework for Java.
- **PostgreSQL**: Relational database for data storage.
- **Maven**: Build and dependency management tool.
- **Lombok**: For reducing boilerplate code.

### Architecture

The backend is structured following a **layered architecture**:

1. **Controllers**: Handle HTTP requests and map them to the appropriate services.
2. **Services**: Contain business logic and interact with repositories.
3. **Repositories**: Interface with the database using Spring Data JPA.
4. **Models**: Represent the database entities.
5. **DTOs**: Data Transfer Objects for transferring data between the layers.
6. **Mappers**: Convert entities to DTOs and vice versa.

### API Endpoints

#### Trips

- `GET /api/trips` - Retrieve all trips.
- `POST /api/trips` - Create a new trip.
- `GET /api/trips/{id}` - Get trip details by ID.
- `PUT /api/trips/{id}` - Update trip details by ID.
- `DELETE /api/trips/{id}` - Delete a trip by ID.
- `POST /api/trips/{id}/expenses` - Add multiple expenses to a trip.

#### Stops

- `GET /api/trips/{tripId}/stops` - Retrieve all stops for a specific trip.
- `GET /api/trips/{tripId}/stops/{stopId}` - Get a specific stop by ID.
- `POST /api/trips/{tripId}/stops` - Add a stop to a specific trip.
- `PUT /api/trips/{tripId}/stops/{stopId}` - Update a stop.
- `DELETE /api/trips/{tripId}/stops/{stopId}` - Delete a stop by ID.

#### Expenses

- `GET /api/expenses/{id}` - Retrieve an expense by ID.
- `GET /api/expenses/trip/{tripId}` - Get all expenses for a specific trip.
- `POST /api/expenses` - Add an expense.
- `PUT /api/expenses/{id}` - Update an expense.
- `DELETE /api/expenses/{id}` - Delete an expense by ID.
- `GET /api/expenses/category/{category}` - Retrieve expenses by category.

#### Categories

- `GET /api/categories` - Retrieve all categories.
- `POST /api/categories` - Create a new category.
- `GET /api/categories/{id}` - Get a category by ID.
- `PUT /api/categories/{id}` - Update a category.
- `DELETE /api/categories/{id}` - Delete a category.
- `GET /api/categories/{id}/trips` - Retrieve all trips associated with a category.

### Future Improvements (Backend)

- **User Authentication and Authorization**: Secure the API with Spring Security and Role-based access control.

## Frontend

The frontend of the **Travel App** is built using **Vue.js** and is currently under development.

### Tech Stack (Frontend)

- **Vue.js 3**: JavaScript framework for building user interfaces.
- **Vue Router**: For handling routing between pages.
- **Axios**: For making HTTP requests to the backend API.
- **Bootstrap**: For styling and responsive design.

### Current Features

- **Dashboard**: Displays an overview of all trips and their details.
- **Create Trip Page**: Allows users to create a new trip with details like title, description, dates, categories, and expenses.
- **View Trip Page**: Shows detailed information about a trip, including its stops and expenses.

### Ongoing Work

- **Edit Trip Page**: A page to edit the details of existing trips is still under development.
- **Expenses Management**: Enhancing functionality to manage expenses more intuitively within the trip view.
- **Reports Page**: Creating a page for generating and viewing reports related to trips, stops, and expenses.

### Future Improvements (Frontend)

- **Edit Page**: Implement editing capabilities for trips, stops, and expenses.
- **Delete Page**: Add functionality to delete trips, stops, and expenses.
- **Reports Page**: Generate detailed reports for trips, including summaries of expenses and activities.
- **Map Integration**: Implement map features to visualize stop locations.
- **User Authentication**: Integrate user authentication and authorization using JWT.


## License

This project is licensed under the MIT License.
