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

### Example Request

```http
POST /api/auth.php
```

```json
{
  "username": "johndoe",
  "email": "johndoe@email.com",
  "password": "password123"
}
```

### Example Response

```json
{
  "status": 200,
  "message": "Logged in as ZenZen!",
  "data": {
    "token": "2a58abbc03adcf08dc778920860933dbecd347b0f3483ba54dca1e71b32dd4f0",
    "user_id": "4a5f77c0-c337-11ef-864c-7c05075eb45f",
    "theme": 1,
    "font_style": "fonts2"
  }
}
```
