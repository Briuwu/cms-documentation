---
title: Posts
sidebar_position: 3
---

## Posts API

The **GreekMyth** project provides a posts API that allows users to create, view, and delete posts. This API ensures secure user authentication with Recaptcha to prevent spam, password recovery with token-based verification, and change password functionality for enhanced account security.

### Base URL

The base URL for the posts API is:

```http
http://localhost/finalProject_ITEC116/GreekMythApi
```

### Endpoints

The posts API provides the following endpoints:

- `GET /api/posts`: Retrieve post information.
- `GET /api/posts/:id`: Retrieve a specific post.
- `POST /api/posts`: Create a new post.
- `DELETE /api/posts/:id`: Delete a specific post.
- `PAGINATION /api/posts`: Retrieve post information with pagination.

### Retrieve Post Information

To retrieve post information, send a `GET` request to the following endpoint:

```http
GET: http://localhost/finalProject_ITEC116/GreekMythApi/api/posts.php
```

### Retrieve a Specific Post

To retrieve a specific post, send a `GET` request to the following endpoint:

```http
GET: http://localhost/finalProject_ITEC116/GreekMythApi/api/posts.php?id=1
```

### Retrieve Post Information with Pagination

To retrieve post information with pagination, send a `GET` request to the following endpoint:

```http
GET: http://localhost/finalProject_ITEC116/GreekMythApi/api/posts.php?page=1&limit=10
```

### Delete a Specific Post

To delete a specific post, send a `DELETE` request to the following endpoint:

```http
DELETE: http://localhost/finalProject_ITEC116/GreekMythApi/api/posts.php?id=1
```

### Create a New Post

To create a new post, send a `POST` request to the following endpoint:

```http
POST: http://localhost/finalProject_ITEC116/GreekMythApi/api/posts.php
```

The request body should contain the following parameters:

- `title`: The title of the post.
- `content`: The content of the post.
- `user_id`: The ID of the user creating the post.
- `greek_id`: The ID of the Greek myth associated with the post.
- `type`: The type of operation to be executed.

### Example Request

```http
POST /api/posts.php
```

```json
{
  "title": "The Story of Zeus",
  "content": "Zeus was the king of the gods and the god of the sky, weather, law and order, destiny and fate, and kingship. He was depicted as a regal",
  "user_id": "1",
  "greek_id": "1",
  "type": "createPost"
}
```

### Example Response

```json
{
  "status": 201,
  "message": "Resource created"
}
```
