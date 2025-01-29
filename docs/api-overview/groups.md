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

- `greek_id`: The ID of the group.
- `name`: The name of the group.
- `description`: The description of the group.
- `image_url`: The URL of the group image.
- `username`: The username of the group creator.

### Example Request

```http
POST /api/groups.php
```

```json
{
  "greek_id": "1779c872-b6b9-11ef-ba98-7c05075eb45f",
  "name": "GreekMyth Fans",
  "description": "A group for fans of GreekMyth!",
  "image_url": "/finalProject_ITEC116/GreekMyth/img/g/67983d9de38740.59562269.jpg",
  "username": "GreekMythAdmin"
}
```

### Example Response

```json
{
  "status": 200,
  "message": "success",
  "data": [
    {
      "greek_id": "0db1bfad-2ba8-11ef-a131-7c05075eb45f",
      "name": "Hermes",
      "description": "Hermes, the quick-witted Greek god of trade, thieves, travelers, sports, athletes, and border crossings, is often portrayed as a young, athletic man wearing a winged hat and sandals. He is known for his cunning and mischievous nature, as well as his role as the messenger of the gods. Hermes is also associated with fertility, luck, and wealth, and is often depicted carrying a caduceus, a winged staff entwined with two serpents.",
      "image_url": "/finalProject_ITEC116/GreekMyth/img/gods/HERMES.webp",
      "creator": "Default",
      "status": 1,
      "username": null,
      "total_people": 4
    },
    {
      "greek_id": "1c87d062-2ba3-11ef-a131-7c05075eb45f",
      "name": "Hades",
      "description": "Hades, in ancient Greek religion, is the god of the underworld. He was a son of the Titans Cronus and Rhea and the brother of Zeus, Poseidon, and Hera. Hades ruled alongside his queen, Persephone, over the dead, although he was not typically a judge or responsible for torturing the guilty\u2014tasks assigned to the Furies",
      "image_url": "/finalProject_ITEC116/GreekMyth/img/gods/HADES.webp",
      "creator": "Default",
      "status": 1,
      "username": null,
      "total_people": 4
    }
  ]
}
```
