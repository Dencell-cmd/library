# library

# Slim PHP API

This API is built using the Slim PHP framework with JWT authentication. It connects to a MySQL database and provides endpoints for interacting with the `library` database.

## Prerequisites

1. **PHP**: Ensure PHP is installed on your machine (v7.4 or higher recommended).
2. **Composer**: Install Composer for dependency management.
3. **MySQL**: Set up a MySQL database with the following details:
   - Database name: `library`
   - Port: `3308`
4. **Thunder Client**: A VS Code extension for API testing.

## Installation

1. Clone the repository or download the `index.php` file.
2. Install dependencies using Composer:
   ```bash

# Endpoints

### 1. User Registration Endpoint
URL: /user/register
Method: POST
Headers:

Content-Type: application/json
Body (JSON):
json
Copy code
{
  "username": "testuser",
  "password": "testpassword"
}

### 2. User Authentication Endpoint
URL: /user/auth
Method: POST
Headers:

Content-Type: application/json
Body (JSON):
json
Copy code
{
  "username": "testuser",
  "password": "testpassword"
}

### 3. Add New Author
URL: /addauthors
Method: POST
Headers:

Content-Type: application/json
Authorization: Bearer <JWT_TOKEN>
Body (JSON):
json
Copy code
{
  "name": "New Author"
}

### 4. Update Author by ID
URL: /authors/{id}
Method: PUT
Headers:

Content-Type: application/json
Authorization: Bearer <JWT_TOKEN>
Body (JSON):
json
Copy code
{
  "name": "Updated Author Name"
}

### 5. Get All Authors
URL: /authors
Method: GET
Headers:

Authorization: Bearer <JWT_TOKEN>

### 6. Add New Book
URL: /addbooks
Method: POST
Headers:

Content-Type: application/json
Authorization: Bearer <JWT_TOKEN>
Body (JSON):
json
Copy code
{
  "title": "New Book Title",
  "author_id": 1
}

### 7. Update Book by ID
URL: /books/{id}
Method: PUT
Headers:

Content-Type: application/json
Authorization: Bearer <JWT_TOKEN>
Body (JSON):
json
Copy code
{
  "title": "Updated Book Title",
  "author_id": 1
}

### 8. Get All Books
URL: /books
Method: GET
Headers:

Authorization: Bearer <JWT_TOKEN>

### 9. Delete Book by ID
URL: /books/{id}
Method: DELETE
Headers:

Authorization: Bearer <JWT_TOKEN>

### 10. Delete Author by ID
URL: /authors/{id}
Method: DELETE
Headers:

Authorization: Bearer <JWT_TOKEN>

