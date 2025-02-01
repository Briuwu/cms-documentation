---
title: Authentication
sidebar_position: 1
---

## Authentication API

The **GreekMyth** project provides an authentication API that allows users to create, view, and delete user accounts. This API ensures secure user authentication with Recaptcha to prevent spam, password recovery with token-based verification, and change password functionality for enhanced account security.

### Base URL

The base URL for the authentication API is:

```http
http://localhost/finalProject_ITEC116/GreekMythApi
```

### Endpoints

The authentication API provides the following endpoints:

- `POST /api/auth/register`: Register a new user account.

#### Register a New User Account

To register a new user account, send a `POST` request to the following endpoint:

```http
POST: http://localhost/finalProject_ITEC116/GreekMythApi/api/auth.php
```

The request body should contain the following parameters:

- `username`: The username of the user.
- `email`: The email address of the user.
- `password`: The password of the user.
- `confirm_password`: The confirmation password of the user.
- `image`: The profile image of the user.
- `Process`: The process to be executed
- `emailVerified`: The email verification status of the user.

### Example Request

```http
POST /api/auth.php
```

```json
{
  "username": "johndoe",
  "email": "johndoe@email.com",
  "password": "password123",
  "confirm_password": "password123",
  "image": "default.jpg",
  "Process": "Register",
  "emailVerified": "true"
}
```

### Example Response

```json
{
  "status": 201,
  "message": "Resource created"
}
```
