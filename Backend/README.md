# RailConnect Backend (Microservices)

The backend for the Train Ticket Booking application is built using Java and Spring Boot. Instead of a monolith, it uses a microservices architecture managed by Netflix Eureka and a Spring Cloud API Gateway.

## Tech Stack

* **Java 8+**
* **Spring Boot (2.7.x)**
* **Spring Cloud:** API Gateway & Netflix Eureka Service Registry.
* **Spring Data JPA / Hibernate:** For database interactions.
* **MySQL:** Relational database for storing user, train, and booking data.
* **Spring Security & JWT:** For securing endpoints and managing user sessions.
* **Maven:** Dependency management.

## Microservices Architecture

The backend consists of the following individual services:

1.  **ticket-booking-service-registry**: The Eureka Server. All other services register themselves here so they can find each other.
2.  **ticket-booking-api-gateway**: The single entry point for the frontend. It routes incoming requests to the appropriate microservice.
3.  **ticket-booking-user-service**: Handles user registration, login authentication, and JWT token generation.
4.  **ticket-booking-location-service**: Manages the train stations/locations.
5.  **ticket-booking-train-service**: Manages the trains, seating capacities, and active schedules.
6.  **ticket-booking-book-service**: Handles the actual ticket booking logic, generating booking references, and interacting with the train service to allocate seats.

## How to Run Locally

### Prerequisites
* Java Development Kit (JDK) installed.
* Maven installed.
* MySQL Server running locally.

### Database Setup
Ensure you have MySQL running. Depending on your `application.properties`/`application.yml` files inside each service, you may need to create the respective databases (e.g., `user_db`, `train_db`, etc.) before starting the application. JPA will automatically generate the tables.

### Running the Services
Because this is a microservices architecture, **the startup order matters.** You should run the applications from your IDE (like IntelliJ or Eclipse) or via Maven in the following order:

1.  Start the **Service Registry** (`TicketBookingServiceRegistryApplication`). Wait for it to initialize.
2.  Start the **API Gateway** (`TicketBookingApiGatewayApplication`).
3.  Start the remaining core services in any order:
    * `TicketBookingUserServiceApplication`
    * `TicketBookingLocationServiceApplication`
    * `TicketBookingTrainServiceApplication`
    * `TicketBookingBookServiceApplication`

If running via terminal, you can navigate into each service folder and run:
```bash
mvn spring-boot:run
```