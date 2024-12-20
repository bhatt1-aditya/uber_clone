# User Registration API Documentation

## Register User

/\*\*

- @description Creates a new user account with the provided information.
  \*/
  Creates a new user account with the provided information.

**Endpoint:** `/users/register`  
/\*\*

- @file README.md
- @description This file contains the documentation for the backend of the UberMern project.
-
- @method POST
  \*/
  **Method:** POST  
  **Content-Type:** application/json

### Request Body

```json
{
  "fullname": {
    "firstname": "string", // required, min 3 characters
    "lastname": "string" // optional, min 3 characters if provided
  },
  "email": "string", // required, min 5 characters, valid email format
  "password": "string" // required, min 6 characters
}
```

### Example Response

```json
{
  "fullname": {
    "firstname": "John",
    "lastname": "Doe"
  },
  "email": "john@example.com",
  "password": "secure123"
}
```

## Login User

Description: Authenticates a user with the provided email and password.

**Endpoint:**` /users/login`
**Method:** POST
**Content-Type:** application/json

### Request Body

```json
{
  "email": "string", // required, valid email format
  "password": "string" // required, min 6 characters
}
```

### Example Response

```json
{
  "token": "jwt_token_string",
  "user": {
    "_id": "user_id",
    "fullname": {
      "firstname": "John",
      "lastname": "Doe"
    },
    "email": "john@example.com"
  }
}
```
