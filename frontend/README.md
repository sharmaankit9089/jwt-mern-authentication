⚛️ Frontend Application (React Client)

This folder contains the React client application responsible for the user interface, routing, and communicating with the MERN backend API.

🔗 Dependencies

    react-router-dom: For routing and private route implementation.

    react-toastify: For displaying notification messages.

📂 Key Files & Logic

File	Description	Core Functionality
src/App.js	Main routing component. Defines the routes and implements the PrivateRoute logic based on the isAuthenticated state.	
src/RefrshHandler.js	Handles authentication checks on page load/refresh. Checks for the JWT in localStorage and sets the global isAuthenticated state, managing redirects from /login, /signup, or / to /home if a token is present.	
src/pages/Signup.js	Handles user registration. Collects name, email, and password, performs basic client-side checks, and sends a POST request to the signup endpoint.	
src/pages/Login.js	Handles user sign-in. Sends a POST request to the login endpoint. On success, it stores the jwtToken and loggedInUser name in localStorage.	
src/pages/Home.js	The protected resource page. It fetches the logged-in user's name and calls the protected /products API, passing the JWT from localStorage in the Authorization header. Includes the Logout button.	

🌐 API Endpoints Consumed

The frontend makes calls to the backend running on http://localhost:8080:
Component	Endpoint	Method	Purpose
Signup.js	/auth/signup	POST	Register a new user.
Login.js	/auth/login	POST	Authenticate user and receive JWT.
Home.js	/products	GET	Fetch protected product data (requires JWT header).
