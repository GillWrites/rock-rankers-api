---
title: "`GET`: retrieve user information"
layout: default
nav_order: 1
parent: "Users Resource"
grand_parent: "API Reference Docs"
permalink: /api-reference-docs/users/get-user/
has_toc: false
description: "Retrieve user information using the `GET` method"
tags:
  - api
categories:
  - api-reference
version: "v1.0"
last_updated: "2025-12-06"
---
<!-- markdownlint-disable MD024 -->

## `GET` retrieve all users

Use the `/users` endpoint to retrieve all user records using the
`GET` method.

### URL

```shell
{server_url}/users
```

  When testing, the {server_url} is the local host:
  <http://localhost:3000/users>.

### Path parameters

| Parameter | Type | Required | Description |
|-----------|------|----------|-------------|
| None | - | - | This endpoint uses the base `/users` path |

### Request headers

| Header | Type | Required | Description |
|--------|------|----------|-------------|
| `Content-Type` | string | No | Not required for GET requests |

### Request body

No request body required for GET requests.

### Request syntax

```bash
curl -X GET http://localhost:3000/users
```

### Response format

Returns an array of user objects, each containing the following
properties:

| Property name | Type | Description |
| ------------- | ----------- | ----------- |
| `id` | integer | Unique identifier assigned by the server |
| `last-name` | string | The user's last name |
| `first-name` | string | The user's first name |
| `email` | string | The user's email address |

### Request example

```bash
curl -X GET http://localhost:3000/users
```

### Response example

```json
[
  {
    "id": 1,
    "last-name": "Renn",
    "first-name": "David",
    "email": "drenn08@uw.edu"
  },
  {
    "id": 2,
    "last-name": "D",
    "first-name": "Gill",
    "email": "gilld@uw.edu"
  },
  {
    "id": 3,
    "last-name": "Watson",
    "first-name": "Bob",
    "email": "bobwatson@uw.edu"
  },
  {
    "id": 4,
    "last-name": "Plan",
    "first-name": "Robert",
    "email": "ledzeppelin@aol.com"
  }
]
```

### Return status

| Status value | Return status | Description |
| ------------- | ----------- | ----------- |
| 200 | Success | All users retrieved successfully |
| ECONNREFUSED | N/A | Service is offline - start the service and try again |

---

## `GET`: retrieve a user by ID

Use the `/users/{id}` endpoint to retrieve a specific user record
using the `GET` method.

### URL

```shell
{server_url}/users/{id}
```

  When testing, the {server_url} is the local host:
  <http://localhost:3000/users/{id}>.

### Path parameters

| Parameter | Type | Required | Description |
|-----------|------|----------|-------------|
| `id` | integer | Yes | The unique identifier of the user to retrieve |

### Request headers

| Header | Type | Required | Description |
|--------|------|----------|-------------|
| `Content-Type` | string | No | Not required for GET requests |

### Request body

No request body required for GET requests.

### Request syntax

```bash
curl -X GET http://localhost:3000/users/{id}
```

### Response format

| Property name | Type | Description |
| ------------- | ----------- | ----------- |
| `id` | integer | Unique identifier assigned by the server |
| `last-name` | string | The user's last name |
| `first-name` | string | The user's first name |
| `email` | string | The user's email address |

### Request example

```bash
curl -X GET http://localhost:3000/users/2
```

### Response example

```json
{
  "id": 2,
  "last-name": "D",
  "first-name": "Gill",
  "email": "gilld@uw.edu"
}
```

### Return status

| Status value | Return status | Description |
| ------------- | ----------- | ----------- |
| 200 | Success | User retrieved successfully |
| 404 | Error | User with specified ID not found |
| ECONNREFUSED | N/A | Service is offline - start the service and try again |

---
