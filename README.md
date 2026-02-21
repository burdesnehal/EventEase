# Geofence Automatic Ticket Validation

## Overview
Geofence Automatic Ticket Validation is a full-stack application designed to automate event ticket validation using geofencing technology. It consists of a Node.js/Express backend and a modern frontend (likely React with Vite), supporting user authentication, event management, booking, and geofence-based ticket validation.

## Features
- User authentication (sign up, login)
- Admin and user dashboards
- Event creation and management
- Ticket booking and validation
- Geofence-based automatic ticket validation
- Responsive frontend UI
- Dockerized frontend and backend for easy deployment

## Project Structure
```
GeofenceAutomaticTicketValidation/
├── backend/         # Node.js/Express backend
│   ├── controllers/ # Route controllers
│   ├── middlewares/ # Express middlewares
│   ├── models/      # Mongoose models
│   ├── routes/      # API routes
│   ├── services/    # Business logic
│   ├── config/      # Configuration files
│   ├── app.js       # Main backend entry
│   ├── Dockerfile   # Backend Docker config
│   └── ...
├── frontend/        # Frontend (Vite + React)
│   ├── src/         # Source code
│   ├── public/      # Static assets
│   ├── Dockerfile   # Frontend Docker config
│   └── ...
├── .gitignore
├── README.md
└── package.json
```

## Getting Started

### Prerequisites
- Node.js (v16+ recommended)
- Docker & Docker Compose (optional, for containerized setup)

### Backend Setup
1. Navigate to the backend folder:
   ```sh
   cd backend
   ```
2. Install dependencies:
   ```sh
   npm install
   ```
3. Configure environment variables in a `.env` file (see `config/db.js` for required variables).
4. Start the backend server:
   ```sh
   npm start
   ```

### Frontend Setup
1. Navigate to the frontend folder:
   ```sh
   cd frontend
   ```
2. Install dependencies:
   ```sh
   npm install
   ```
3. Start the frontend development server:
   ```sh
   npm run dev
   ```

### Docker Setup (Optional)
1. From the project root, run:
   ```sh
   docker-compose up --build
   ```
   This will build and start both frontend and backend containers.

## Usage
- Access the frontend at `http://localhost:3000` (or as configured)
- Backend API runs at `http://localhost:5000` (or as configured)
- Register/login as a user or admin
- Admins can create/manage events
- Users can book tickets and validate them via geofence

## Folder Details
- **backend/controllers/**: Handles API logic
- **backend/models/**: Mongoose schemas for MongoDB
- **backend/routes/**: Express route definitions
- **backend/services/**: Business logic and helpers
- **frontend/src/pages/**: Main app pages (Home, Login, Dashboard, etc.)
- **frontend/src/components/**: Reusable UI components

## Contributing
Pull requests are welcome! For major changes, please open an issue first to discuss what you would like to change.

## License
[MIT](LICENSE)

## Authors
- Sneha Burde
- [Your Name Here]
