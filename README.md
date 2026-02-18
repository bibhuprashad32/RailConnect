# RailConnect - Train Ticket Booking System

A full-stack web application for booking train tickets. This project allows users to search for scheduled trains, book tickets, and view their booking history. It also includes an admin module for managing trains, stations, and scheduling.

The application is built using a microservices architecture to separate different business domains.

## Project Structure

This repository is divided into two main parts:

* **`/Frontend`**: Contains the React.js user interface.
* **`/Backend`**: Contains the Java Spring Boot microservices and API Gateway.

## High-Level Features

* **Role-Based Access:** Separate interfaces and permissions for Admins and Customers.
* **Train Management:** Admins can add locations (stations), trains, and create train schedules.
* **Booking System:** Customers can search for trains between locations on specific dates and book tickets.
* **Microservices Backend:** The backend is split into dedicated services (User, Train, Location, Booking) managed by an API Gateway and Service Registry.

## Getting Started

To run this project locally, you will need to start the backend microservices and the frontend development server separately. 

* For frontend setup instructions, see the [Frontend README](./Frontend/README.md).
* For backend setup instructions, see the [Backend README](./Backend/README.md).