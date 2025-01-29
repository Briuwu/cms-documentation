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

### Delete a Specific User Account

To delete a specific user account, send a `DELETE` request to the following endpoint:

```http
DELETE: http://localhost/finalProject_ITEC116/GreekMythApi/api/users.php?id=1
```

### Example Request

```http
GET /api/users.php
```

```json
{
  "username": "DaeWae",
  "email": "wae@gmail.com",
  "password": "password123"
}
```

### Example Response

```json
{
  "status": 200,
  "message": "success",
  "data": [
    {
      "user_id": "1779c872-b6b9-11ef-ba98-7c05075eb45f",
      "username": "DaeWae",
      "email": "wae@gmail.com",
      "joined_at": "2024-12-10 13:39:15",
      "profile_pic": "/finalProject_ITEC116/GreekMyth/img/u/67983d9de38740.59562269.jpg",
      "bio": "Hello GreekMyth!",
      "totalFriends": 3
    }
  ]
}
```
