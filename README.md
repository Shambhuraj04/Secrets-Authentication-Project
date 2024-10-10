# Secret Sharing App

This project is a web application built using Node.js and Express, designed to allow users to share and store personal secrets securely. It features user authentication via local strategies and Google OAuth, enabling users to register, log in, and submit their secrets.

## Features

- User registration and authentication
- Secure password storage with bcrypt
- Google OAuth for easy login
- User-specific secret storage
- Responsive user interface using EJS for templating

## Technologies Used

- Node.js
- Express.js
- PostgreSQL
- Passport.js (for authentication)
- Bcrypt (for password hashing)
- Google OAuth 2.0
- dotenv (for environment variable management)
- EJS (for templating)

## Prerequisites

Make sure you have the following installed:

- Node.js (version 14 or later)
- PostgreSQL (installed and running)
- A Google Cloud project with OAuth 2.0 credentials

## Getting Started

1. **Clone the repository:**

   ```bash
   git clone <repository-url>
   cd <repository-folder>

2. **Install the dependencies:**

    ```bash
    npm install

3. **Set up environment variables:**

    Create a .env file in the root directory and add the following variables:

    ```plaintext
    SESSION_SECRET=your_session_secret
    PG_USER=your_postgres_user
    PG_HOST=localhost
    PG_DATABASE=your_database_name
    PG_PASSWORD=your_postgres_password
    PG_PORT=5432
    GOOGLE_CLIENT_ID=your_google_client_id
    GOOGLE_CLIENT_SECRET=your_google_client_secret
    Set up your PostgreSQL database:

4. **Create a database and a users table with the following structure:**

    ```sql
    CREATE TABLE users (
    id SERIAL PRIMARY KEY,
    username VARCHAR(255) UNIQUE NOT NULL,
    password VARCHAR(255),
    secret TEXT
    );

5. **Run the application:**

    ```bash
    npm start

  The server will start on http://localhost:3000.

6. **Access the application:**

     Open your browser and navigate to http://localhost:3000. You can register a new account or log in using your Google account.

## Usage
- Home Page: Displays the application welcome message.
- Login: Allows users to log in using their credentials or Google account.
- Register: New users can create an account here.
- Secrets: Authenticated users can view their secrets. If no secret exists, a prompt will ask for input.
- Submit: Authenticated users can submit a new secret, which will be stored in the database.

## Contributing
  Contributions are welcome! If you'd like to contribute, please fork the repository and submit a pull request.




