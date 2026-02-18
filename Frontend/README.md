# RailConnect Frontend

This is the user interface for the Train Ticket Booking application, built using React. 

## Tech Stack

* **React.js** (Bootstrapped with Create React App)
* **React Router DOM:** For navigating between pages (booking, admin dashboard, login, etc.)
* **Axios:** For making HTTP requests to the backend API Gateway.
* **React Toastify:** For displaying UI success/error notifications.

## Features

* **User Authentication:** Login and Registration forms for customers.
* **Customer Dashboard:** Search for trains, book tickets, and view personal booking history.
* **Admin Dashboard:** Interfaces to add new trains, manage locations, and schedule train routes.
* **Dynamic Navbars:** The navigation menu changes based on whether the user is logged in as an Admin or a Customer.

## How to Run Locally

### Prerequisites
* Node.js and npm installed on your machine.
* The backend microservices must be running for data fetching to work.

### Steps
1. Open your terminal and navigate to the `Frontend` folder.
2. Install the dependencies: `npm install`
3. Start the development server: `npm start`

The app will automatically open in your browser at http://localhost:3000.

To make this site work properly, please ensure the backend server is running properly.