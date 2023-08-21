# Flutter Assessment API Documentation

Welcome to the API documentation for the Flutter assessment.
This document outlines the REST API endpoints and their usage to facilitate the development of your Flutter app.

## Base URL

The base URL for all API endpoints is: `https://eram-flutter-assessment-backend.onrender.com`

## Endpoints

### 1. List Todos

- **Endpoint**: `/todos`
- **Method**: GET
- **Description**: Retrieve a list of all todos.
- **Response**: JSON array containing todo objects.

  ```json
  [
    {
      "id": 1,
      "title": "Buy groceries",
      "completed": false
    },
    {
      "id": 2,
      "title": "Finish coding challenge",
      "completed": true
    }
  ]
  ```

### 2. Create Todo

- **Endpoint**: `/todos`
- **Method**: POST
- **Description**: Create a new todo.
- **Request Body**:

  ```json
  {
    "title": "New task"
  }
  ```

- **Response**: JSON object representing the created todo.

  ```json
  {
    "id": 3,
    "title": "New task",
    "completed": false
  }
  ```

### 3. Update Todo

- **Endpoint**: `/todos/{id}`
- **Method**: PUT
- **Description**: Update an existing todo by ID.
- **Request Body**:

  ```json
  {
    "title": "Updated task",
    "completed": true
  }
  ```

- **Response**: JSON object representing the updated todo.

  ```json
  {
    "id": 3,
    "title": "Updated task",
    "completed": true
  }
  ```

### 4. Delete Todo

- **Endpoint**: `/todos/{id}`
- **Method**: DELETE
- **Description**: Delete a todo by ID.
- **Response**: No response body. HTTP status 204 on success.

## Error Handling

In case of errors, the API will return an error response with appropriate status codes and error messages.

- **Status Code 400**: Bad Request - Invalid request or missing data.
- **Status Code 404**: Not Found - Resource not found.
- **Status Code 500**: Internal Server Error - An unexpected error occurred on the server.
