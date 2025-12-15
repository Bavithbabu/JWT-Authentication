# Go JWT Authentication API

A RESTful API built with Go, Gin framework, and MongoDB for user authentication using JWT tokens.

## Features

- User signup and login
- JWT token-based authentication
- Password hashing with bcrypt
- Role-based access control (USER/ADMIN)
- MongoDB Atlas integration
- Protected routes with middleware

## Tech Stack

- **Language:** Go 1.23
- **Framework:** Gin
- **Database:** MongoDB Atlas
- **Authentication:** JWT (JSON Web Tokens)
- **Validation:** go-playground/validator

## API Endpoints

### Public Routes
- `POST /users/signup` - Register new user
- `POST /users/login` - Login user

### Protected Routes (Require Token)
- `GET /users` - Get all users (ADMIN only)
- `GET /users/:user_id` - Get specific user
- `GET /api-1` - Test endpoint
- `GET /api-2` - Test endpoint

## Setup

1. Clone the repository:
```bash
git clone https://github.com/YOUR_USERNAME/Go-lang-JWT.git
cd Go-lang-JWT
```

2. Install dependencies:
```bash
go mod download
```

3. Create `.env` file:
```env
PORT=9000
MONGODB_URI=your_mongodb_connection_string
SECRET_KEY=your_secret_key
```

4. Run the application:
```bash
go run main.go
```

## Environment Variables

- `PORT` - Server port (default: 8080)
- `MONGODB_URI` - MongoDB connection string
- `SECRET_KEY` - Secret key for JWT signing

## Project Structure

```
Go-lang-JWT/
├── controllers/      # Request handlers
├── database/         # Database connection
├── helpers/          # Helper functions (JWT, auth)
├── middleware/       # Authentication middleware
├── models/           # Data models
├── routes/           # Route definitions
├── main.go           # Entry point
├── go.mod            # Go modules
└── .env              # Environment variables
```

## Author

Bavith Babu

## License

MIT
