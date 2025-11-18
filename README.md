🔑 MERN Stack Authentication & Product Listing

This is a complete MERN (MongoDB, Express, React, Node.js) stack application demonstrating full-featured User Authentication (Signup and Login) using JSON Web Tokens (JWT) and protected routing.

The project structure is split into two main directories: frontend (React client) and backend (Node.js/Express server).

🌟 Features

    Full User Authentication: Secure Signup and Login using hashed passwords and JWT.

    Secure Routing: Implements Private Routing on the client-side to protect the Home page.

    Protected Resources: Uses JWT Middleware on the server to restrict access to the /products endpoint.

    Token Management: JWT is stored in localStorage for session persistence.

    Client-Side Redirection: Manages automatic redirection for authenticated users on refresh or direct URL access.

    Validation: Includes both client-side and server-side validation (using Joi, as discussed in the associated tutorial).

    Technology: Developed following the structure outlined in the tutorial: "Complete Login/Signup MERN Stack | Mongo, Express, React and Node Authentication with Deployment".

💻 Tech Stack

Component	Technology	Details
Frontend	React	Routing (react-router-dom), State Management (useState, useEffect), Notifications (react-toastify).
Backend	Node.js, Express	Server setup, API endpoints, Middleware.
Database	MongoDB	Data storage for Users and Products (via Mongoose).
Authentication	JWT, bcrypt	JSON Web Tokens for authorization; bcrypt for password hashing.
Validation	Joi	Library for server-side schema validation.

⚙️ Setup and Installation

Follow the steps below to set up and run the application locally.

1. Backend Setup

Navigate to the backend directory and follow its setup instructions. You will need to set up a MongoDB connection and environment variables.
Bash

cd backend
npm install
# Configure .env file (see backend README)
npm start

2. Frontend Setup

Navigate to the frontend directory and follow its setup instructions.
Bash

cd frontend
npm install
npm start

The client application will typically open in your browser at https://jwt-mern-authentication-ui.vercel.app/login , and will connect to the backend running on https://jwt-mern-authentication-api.vercel.app/.
