## Overview
The Planetary API is a Flask-based RESTful API for managing planetary data and user information. It provides endpoints for CRUD operations on planets and supports user authentication and password retrieval using JWT and email services. The application uses SQLite as the database and includes sample data for testing purposes.

## Features
User Management
Register users
User login with JWT token generation
Password retrieval via email
Planetary Data Management
Add, update, delete, and view planetary information
Authentication
Secured endpoints using JWT
Email Notifications
Send password recovery emails
Database Commands
Create, drop, and seed the database using CLI commands

## API Endpoints
### User Endpoints

| Endpoint                 | Method | Description                               |
|--------------------------|--------|-------------------------------------------|
| `/register`              | POST   | Register a new user.                     |
| `/login`                 | POST   | User login, returns a JWT.               |
| `/retrieve_password/<email>` | GET    | Sends the user's password via email.     |

### Planet Endpoints

| Endpoint                  | Method | Description                               |
|---------------------------|--------|-------------------------------------------|
| `/planets`                | GET    | Retrieves a list of all planets.         |
| `/planet_details/<planet_id>` | GET    | Retrieves details of a specific planet.  |
| `/add_planet`             | POST   | Adds a new planet (requires JWT).        |
| `/update_planet`          | PUT    | Updates an existing planet (requires JWT). |
| `/remove_planet/<planet_id>` | DELETE | Deletes a planet (requires JWT).         |
