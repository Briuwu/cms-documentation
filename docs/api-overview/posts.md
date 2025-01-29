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

- `user_id`: The ID of the user creating the post.
- `post_id`: The ID of the post.
- `title`: The title of the post.
- `content`: The content of the post.

### Example Request

```http
POST /api/posts.php
```

```json
{
  "user_id": "1779c872-b6b9-11ef-ba98-7c05075eb45f",
  "post_id": "9478ef85-dd16-11ef-a84b-7c05075eb45f",
  "title": "Hello GreekMyth!",
  "content": "This is my first post on GreekMyth. Excited to share my thoughts with the community!"
}
```

### Example Response

```json
{
  "status": 200,
  "message": "success",
  "data": [
    {
      "post_id": "9478ef85-dd16-11ef-a84b-7c05075eb45f",
      "username": "DaeWae",
      "title": "Hello",
      "content": "Hello Gys",
      "created_at": "2025-01-28 09:24:11",
      "likes": 0,
      "dislikes": 0,
      "status": 1,
      "name": "Artemis"
    },
    {
      "post_id": "354e6eb4-dcbf-11ef-96dd-7c05075eb45f",
      "username": "ChouIsOP",
      "title": "Hello Goddsssss",
      "content": "",
      "created_at": "2025-01-27 22:58:46",
      "likes": 1,
      "dislikes": 0,
      "status": 1,
      "name": "Apollo"
    },
    {
      "post_id": "95fa0fb6-dcb8-11ef-96dd-7c05075eb45f",
      "username": "Administrator",
      "title": "The is a second test post",
      "content": "Test",
      "created_at": "2025-01-27 22:11:22",
      "likes": 1,
      "dislikes": 0,
      "status": 1,
      "name": "Aphrodite"
    },
    {
      "post_id": "95c8dc12-dcb8-11ef-96dd-7c05075eb45f",
      "username": "Administrator",
      "title": "The is a second test post",
      "content": "Test",
      "created_at": "2025-01-27 22:11:21",
      "likes": 1,
      "dislikes": 1,
      "status": 1,
      "name": "Aphrodite"
    },
    {
      "post_id": "64d91674-c72a-11ef-8716-7c05075eb45f",
      "username": "ChouIsOP",
      "title": "asdasdasd",
      "content": "asdsad",
      "created_at": "2024-12-31 11:50:36",
      "likes": 2,
      "dislikes": 0,
      "status": 0,
      "name": null
    }
  ]
}
```
