---
title: "`GET`: retrieve band information"
layout: default
nav_order: 1
parent: "Bands Resource"
grand_parent: "API Reference Docs"
permalink: /api-reference-docs/bands/get-band/
has_toc: false
description: "Retrieve band information using the `GET` method"
tags:
  - api
categories:
  - api-reference
version: "v1.0"
last_updated: "2025-12-06"
---
<!-- markdownlint-disable MD024 -->

## `GET` retrieve all bands

Use the `/bands` endpoint to retrieve all band records using the `GET`
method.

### URL

```shell
{server_url}/bands
```

  When testing, the {server_url} is the local host:
  <http://localhost:3000/bands>.

### Path parameters

| Parameter | Type | Required | Description |
|-----------|------|----------|-------------|
| None | - | - | This endpoint uses the base `/bands` path |

### Request headers

| Header | Type | Required | Description |
|--------|------|----------|-------------|
| `Content-Type` | string | No | Not required for GET requests |

### Request body

No request body required for GET requests.

### Request syntax

```bash
curl -X GET http://localhost:3000/bands
```

### Response format

Returns an array of band objects, each containing the following
properties:

| Property name | Type | Description |
| ------------- | ----------- | ----------- |
| `id` | integer | Unique identifier assigned by the server |
| `name` | string | The band name |
| `genre` | string | The band genre |
| `years-active` | string | The years the band was/is active |
| `origin` | string | The origin location of the band |

### Request example

```bash
curl -X GET http://localhost:3000/bands
```

### Response example

```json
[
  {
    "id": 1,
    "name": "The Beatles",
    "genre": "rock, pop, psychedelia",
    "years-active": "1960-1970",
    "origin": "Liverpool, England"
  },
  {
    "id": 2,
    "name": "Led Zeppelin",
    "genre": "rock, blues, folk, metal",
    "years-active": "1968-1980",
    "origin": "London, England"
  },
  {
    "id": 3,
    "name": "Radiohead",
    "genre": "rock, alternative, electronica",
    "years-active": "1985-present",
    "origin": "Abingdon, Oxfordshire, England"
  },
  {
    "id": 4,
    "name": "Rage Against the Machine",
    "genre": "rock, alternative, metal, rap, funk",
    "years-active": "1991-2000; 2008-2011; 2019-2024",
    "origin": "Los Angeles, California, USA"
  },
  {
    "id": 5,
    "name": "Soundgarden",
    "genre": "rock, alternative, grunge",
    "years-active": "1984-1997; 2010-2017",
    "origin": "Seattle, Washington, USA"
  }
]
```

### Return status

| Status value | Return status | Description |
| ------------- | ----------- | ----------- |
| 200 | Success | All bands retrieved successfully |
| ECONNREFUSED | N/A | Service is offline - start the service and try again |

---

## `GET`: retrieve a band by ID

Use the `/bands/{id}` endpoint to retrieve a specific band record using
the `GET` method.

### URL

```shell
{server_url}/bands/{id}
```

  When testing, the {server_url} is the local host:
  <http://localhost:3000/bands/{id}>.

### Path parameters

| Parameter | Type | Required | Description |
|-----------|------|----------|-------------|
| `id` | integer | Yes | The unique identifier of the band to retrieve |

### Request headers

| Header | Type | Required | Description |
|--------|------|----------|-------------|
| `Content-Type` | string | No | Not required for GET requests |

### Request body

No request body required for GET requests.

### Request syntax

```bash
curl -X GET http://localhost:3000/bands/{id}
```

### Response format

| Property name | Type | Description |
| ------------- | ----------- | ----------- |
| `id` | integer | Unique identifier assigned by the server |
| `name` | string | The band name |
| `genre` | string | The band genre |
| `years-active` | string | The years the band was/is active |
| `origin` | string | The origin location of the band |

### Request example

```bash
curl -X GET http://localhost:3000/bands/2
```

### Response example

```json
{
  "id": 2,
  "name": "Led Zeppelin",
  "genre": "rock, blues, folk, metal",
  "years-active": "1968-1980",
  "origin": "London, England"
}
```

### Return status

| Status value | Return status | Description |
| ------------- | ----------- | ----------- |
| 200 | Success | Band retrieved successfully |
| 404 | Error | Band with specified ID not found |
| ECONNREFUSED | N/A | Service is offline - start the service and try again |

---
