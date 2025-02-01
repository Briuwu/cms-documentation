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
- `PAGINATION /api/comments`: Retrieve comment information with pagination.

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

### Retrieve Comment Information with Pagination

To retrieve comment information with pagination, send a `GET` request to the following endpoint:

```http
GET: http://localhost/finalProject_ITEC116/GreekMythApi/api/comments.php?page=1&limit=10
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

- `user_id`: The ID of the user creating the comment.
- `post_id`: The ID of the post the comment is associated with.
- `parent_id`: The ID of the parent comment (if any).
- `content`: The content of the comment.
- `type`: The type of request (`createComment`).

### Example Request

```http
POST /api/comments.php
```

```json
{
  "user_id": 1,
  "post_id": 1,
  "parent_id": 1,
  "content": "This is a comment.",
  "type": "createComment"
}
```

### Example Response

```json
{
  "status": 201,
  "message": "Resource created"
}
```
