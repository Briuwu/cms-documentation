---
title: Groups
sidebar_position: 4
---

## Groups API

The **GreekMyth** project provides a groups API that allows users to create, view, and delete groups. This API ensures secure user authentication with Recaptcha to prevent spam, password recovery with token-based verification, and change password functionality for enhanced account security.

### Base URL

The base URL for the groups API is:

```http
http://localhost/finalProject_ITEC116/GreekMythApi
```

### Endpoints

The groups API provides the following endpoints:

- `GET /api/groups`: Retrieve group information.
- `GET /api/groups/:id`: Retrieve a specific group.
- `POST /api/groups`: Create a new group.
- `DELETE /api/groups/:id`: Delete a specific group.
- `PAGINATION /api/groups`: Retrieve group information with pagination.

### Retrieve Group Information

To retrieve group information, send a `GET` request to the following endpoint:

```http
GET: http://localhost/finalProject_ITEC116/GreekMythApi/api/groups.php
```

### Retrieve a Specific Group

To retrieve a specific group, send a `GET` request to the following endpoint:

```http
GET: http://localhost/finalProject_ITEC116/GreekMythApi/api/groups.php?id=1
```

### Retrieve Group Information with Pagination

To retrieve group information with pagination, send a `GET` request to the following endpoint:

```http
GET: http://localhost/finalProject_ITEC116/GreekMythApi/api/groups.php?page=1&limit=10
```

### Delete a Specific Group

To delete a specific group, send a `DELETE` request to the following endpoint:

```http
DELETE: http://localhost/finalProject_ITEC116/GreekMythApi/api/groups.php?id=1
```

### Create a New Group

To create a new group, send a `POST` request to the following endpoint:

```http
POST: http://localhost/finalProject_ITEC116/GreekMythApi/api/groups.php
```

The request body should contain the following parameters:

- `creator`: The creator of the group.
- `name`: The name of the group.
- `description`: The description of the group.
- `image`: The image of the group.
- `type`: The type of operation to be performed.

### Example Request

```http
POST /api/groups.php
```

```json
{
  "creator": "Default",
  "name": "Olympian Gods",
  "description": "The Olympian Gods are a group of twelve gods who ruled the world after the Titans. They are the principal deities of the Greek pantheon, residing atop Mount Olympus. The Olympian Gods are associated with various aspects of life, such as love, war, wisdom, and the sea.",
  "image": "olympian_gods.jpg",
  "type": "createGroup"
}
```

### Example Response

```json
{
  "status": 201,
  "message": "Resource created"
}
```
