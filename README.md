# UAS-CRUD Application

## Overview
This is a full-stack application built with React.js and Node.js, designed to manage user authentication with features including user registration, login, profile management, and account deletion. Additional features like email verification and password reset are also implemented.

## Front-End

### Setup
- Initialize a new React.js project using Create React App.
- Utilize React Router for handling client-side routing.

### Components
- **Home Component**: Landing page with links to "Login" and "Sign Up".
- **Login Component**: Form for users to log in.
- **Sign Up Component**: Form for users to create a new account.
- **Profile Component**: Display user profile information with options to update or delete the account.

### Features
- **User Registration**: Allow users to register for a new account.
- **User Login**: Allow users to log in using their email and password.
- **User Profile**: Display the user's profile information.
- **Update Profile**: Allow users to update their profile information.
- **Delete Account**: Allow users to delete their account.

### State Management
- Utilize React Context or a state management library like Redux for managing the authentication state (logged-in user, JWT token).

### Styling
- Style components using CSS or any framework like Bootstrap, SCSS, or Tailwind CSS.

## Back-End

### Setup
- Initialize a new Node.js project with Express.
- Use MongoDB with Mongoose for data storage or any other relevant database (PostgreSQL or MySQL).
- Implement bcrypt for password hashing.
- Employ JSON Web Tokens (JWT) for authentication.

### API Endpoints
- `POST /api/auth/signup`: Register a new user.
- `POST /api/auth/login`: Authenticate a user and return a JWT.
- `GET /api/auth/profile`: Retrieve the authenticated user's profile information.
- `PUT /api/auth/profile`: Update the authenticated user's profile information.
- `DELETE /api/auth/profile`: Delete the authenticated user's account.

### User Model
- For PostgreSQL, MySQL, or any other database solution, create a user schema incorporating fields like name, email, password, and any additional relevant data.

## Bonus Features (Optional)
- Implement email verification during the registration process.
- Add password reset functionality.
- Implement role-based access control (e.g., admin and user roles) if possible.
- Implement pagination and filtering for the list of users (for admin users).

## Installation

### Front-End
1. Initialize React app:
    ```bash
    npx create-react-app client
    ```
2. Navigate to the client directory:
    ```bash
    cd client
    ```
3. Install required dependencies:
    ```bash
    npm install react-router-dom axios
    ```

### Back-End
1. Initialize Node.js project:
    ```bash
    npm init -y
    ```
2. Install required dependencies:
    ```bash
    npm install express mongoose bcryptjs jsonwebtoken nodemailer
    ```

## Running the Application Locally

### Starting the Back-End
1. Ensure MongoDB is running on your machine or set up a remote MongoDB connection.
2. Create a file named `.env` in the root of your back-end project with the following contents:
    ```env
    PORT=5000
    MONGO_URI=your_mongodb_connection_string
    JWT_SECRET=your_jwt_secret
    EMAIL_USER=your_email@example.com
    EMAIL_PASS=your_email_password
    ```
3. Start the back-end server:
    ```bash
    node index.js
    ```

### Starting the Front-End
1. Navigate to the `client` directory:
    ```bash
    cd client
    ```
2. Start the front-end development server:
    ```bash
    npm start
    ```

### Accessing the Application
- Open your browser and go to `http://localhost:3000` to access the front-end.
- The back-end API will be running on `http://localhost:5000`.

