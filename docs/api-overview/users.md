---
title: Users
sidebar_position: 2
---

## Users API

The **GreekMyth** project provides a users API that allows users to create, view, and delete user accounts. This API ensures secure user authentication with Recaptcha to prevent spam, password recovery with token-based verification, and change password functionality for enhanced account security.

### Base URL

The base URL for the users API is:

```http
http://localhost/finalProject_ITEC116/GreekMythApi
```

### Endpoints

The users API provides the following endpoints:

- `GET /api/users`: Retrieve user account information.
- `GET /api/users/:id`: Retrieve a specific user account.
- `DELETE /api/users/:id`: Delete a specific user account.
- `PAGINATION /api/users`: Retrieve user account information with pagination.

### Retrieve User Account Information

To retrieve user account information, send a `GET` request to the following endpoint:

```http
GET: http://localhost/finalProject_ITEC116/GreekMythApi/api/users.php
```

### Retrieve a Specific User Account

To retrieve a specific user account, send a `GET` request to the following endpoint:

```http
GET: http://localhost/finalProject_ITEC116/GreekMythApi/api/users.php?id=1
```

### Retrieve User Account Information with Pagination

To retrieve user account information with pagination, send a `GET` request to the following endpoint:

```http
GET: http://localhost/finalProject_ITEC116/GreekMythApi/api/users.php?page=1&limit=10
```

### Delete a Specific User Account

To delete a specific user account, send a `DELETE` request to the following endpoint:

```http
DELETE: http://localhost/finalProject_ITEC116/GreekMythApi/api/users.php?id=1
```

### Create a New User Account

To create a new user account, send a `POST` request to the following endpoint:

```http
POST: http://localhost/finalProject_ITEC116/GreekMythApi/api/users.php
```

The request body should contain the following parameters:

- `username`: The username of the user.
- `email`: The email address of the user.
- `password`: The password of the user.
- `confirmPassword`: The confirmation password of the user.
- `image`: The profile image of the user.
- `bio`: The biography of the user.
- `Process`: The process to be executed

### Example Request

```http
GET /api/users.php
```

```json
{
  "username": "DaeWae",
  "password": "password123",
  "email": "DaeWae@email.com",
  "confirmPassword": "password123",
  "image": "default.jpg",
  "bio": "Hello GreekMyth!",
  "Process": "createUser"
}
```

### Example Response

```json
{
  "status": 201,
  "message": "Resource created"
}
```
