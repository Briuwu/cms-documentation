---
title: Comments
sidebar_position: 5
---

## Comments API

The **GreekMyth** project provides a comments API that allows users to create, view, and delete commets. This API ensures secure user authentication with Recaptcha to prevent spam, password recovery with token-based verification, and change password functionality for enhanced account security.

### Base URL

The base URL for the comments API is:

```http
http://localhost/finalProject_ITEC116/GreekMythApi
```

### Endpoints

The comments API provides the following endpoints:

- `GET /api/comments`: Retrieve comment information.
- `GET /api/comments/:id`: Retrieve a specific comment.
- `POST /api/comments`: Create a new comment.
- `DELETE /api/comments/:id`: Delete a specific comment.

### Retrieve Comment Information

To retrieve comment information, send a `GET` request to the following endpoint:

```http
GET: http://localhost/finalProject_ITEC116/GreekMythApi/api/comments.php
```

### Retrieve a Specific Comment

To retrieve a specific comment, send a `GET` request to the following endpoint:

```http
GET: http://localhost/finalProject_ITEC116/GreekMythApi/api/comments.php?id=1
```

### Delete a Specific Comment

To delete a specific comment, send a `DELETE` request to the following endpoint:

```http
DELETE: http://localhost/finalProject_ITEC116/GreekMythApi/api/comments.php?id=1
```

### Create a New Comment

To create a new comment, send a `POST` request to the following endpoint:

```http
POST: http://localhost/finalProject_ITEC116/GreekMythApi/api/comments.php
```

The request body should contain the following parameters:

- `content`: The content text.
- `user_id`: The ID of the user who posted the comment.
- `post_id`: The ID of the post the comment is associated with.
- `title`: The title of the post the comment is associated with.

### Example Request

```http
POST /api/comments.php
```

```json
{
  "content": "This is a comment.",
  "user_id": "4a5f77c0-c337-11ef-864c-7c05075eb45f",
  "post_id": "4a5f77c0-c337-11ef-864c-7c05075eb45f",
  "title": "The is a second test post"
}
```

### Example Response

```json
{
  "status": 200,
  "message": "success",
  "data": [
    {
      "comment_id": "6797a9cad05eb",
      "title": "The is a second test post",
      "username": "Administrator",
      "content": "This is a comment.",
      "created_at": "2025-01-27 22:11:22",
      "likes": 0,
      "dislikes": 0,
      "status": 1,
      "name": "Aphrodite"
    }
  ]
}
```
