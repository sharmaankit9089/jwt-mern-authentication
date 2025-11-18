⚙️ Backend README (/backend directory)

🌐 Backend Application (Node.js/Express Server)

This folder contains the server-side code for the MERN application, providing the necessary APIs for user authentication and protected resource access.

🛠️ Technology & Dependencies

    Express: Web framework for Node.js.

    Mongoose: MongoDB object modeling tool.

    jsonwebtoken (JWT): For creating and verifying authentication tokens.

    bcrypt: For securely hashing and comparing user passwords.

    Joi: For server-side input validation and schema definition.

    dotenv: For managing environment variables (like MongoDB URI and JWT Secret).

    cors: To allow cross-origin requests from the React frontend running on a different port.

🔒 Authentication Flow

    Signup: User data is received, password is hashed using bcrypt, and the user is saved to MongoDB.

    Login: User email and password are checked against the database. The submitted password is compared to the stored hash. If valid, a JWT is signed and returned to the client.

    Protected Route Access: All requests to protected routes (like /products) pass through the EnsureAuthenticated middleware. This middleware verifies the JWT from the Authorization header. If the token is valid, the request proceeds; otherwise, a 403 Unauthorised response is returned.

📍 API Endpoints

The server exposes the following routes, typically under the base URL http://localhost:8080:
Endpoint	Method	Access	Description
/auth/signup	POST	Public	Registers a new user. Requires name, email, password.
/auth/login	POST	Public	Logs in a user. Requires email, password. Returns jwtToken and name on success.
/products	GET	Protected	Returns a list of products. Requires a valid JWT in the Authorization header.

⚙️ Setup

    Install dependencies:
    Bash

npm install express mongoose jsonwebtoken bcrypt joi dotenv cors

Create .env file: Create a file named .env in the root of the backend directory and add the following variables:

PORT=8080
MONGO_CONN="mongodb+srv://sharmaankit9089_db_user:SK4wzyOQR7h9916T@cluster0.iggrrbs.mongodb.net/auth-db?appName=Cluster0"
JWT_SECRET="secret-123"

Run the server:
Bash

npm start
