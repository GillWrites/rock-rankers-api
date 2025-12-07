---
title: "`GET`: retrieve album information"
layout: default
nav_order: 1
parent: "Albums Resource"
grand_parent: "API Reference Docs"
permalink: /api-reference-docs/albums/get-album/
has_toc: false
description: "Retrieve album information using the `GET` method"
tags:
  - api
categories:
  - api-reference
version: "v1.0"
last_updated: "2025-12-06"
---
<!-- markdownlint-disable MD024 -->

## `GET` retrieve all albums

Use the `/albums` endpoint to retrieve all album records using the
`GET` method.

### URL

```shell
{server_url}/albums
```

  When testing, the {server_url} is the local host:
  <http://localhost:3000/albums>.

### Path parameters

| Parameter | Type | Required | Description |
|-----------|------|----------|-------------|
| None | - | - | This endpoint uses the base `/albums` path |

### Request headers

| Header | Type | Required | Description |
|--------|------|----------|-------------|
| `Content-Type` | string | No | Not required for GET requests |

### Request body

No request body required for GET requests.

### Request syntax

```bash
curl -X GET http://localhost:3000/albums
```

### Response format

Returns an array of album objects, each containing the following
properties:

| Property name | Type | Description |
| ------------- | ----------- | ----------- |
| `id` | integer | Unique identifier assigned by the server |
| `name` | string | The band name |
| `album` | string | The album name |
| `release-date` | integer | The album release year |
| `album-score` | integer | The album score |
| `global-album-ranking` | integer | The global ranking of the album |
| `band-catalog-album-ranking` | integer | The ranking within the band's catalog |

### Request example

```bash
curl -X GET http://localhost:3000/albums
```

### Response example

```json
[
  {
    "id": 1,
    "name": "The Beatles",
    "album": "Rubber Soul",
    "release-date": 1965,
    "album-score": 987,
    "global-album-ranking": 3,
    "band-catalog-album-ranking": 3
  },
  {
    "id": 2,
    "name": "Led Zeppelin",
    "album": "Led Zeppelin I",
    "release-date": 1969,
    "album-score": 961,
    "global-album-ranking": 2,
    "band-catalog-album-ranking": 1
  },
  {
    "id": 3,
    "name": "Radiohead",
    "album": "Ok Computer",
    "release-date": 1997,
    "album-score": 955,
    "global-album-ranking": 3,
    "band-catalog-album-ranking": 1
  },
  {
    "id": 4,
    "name": "Rage Against the Machine",
    "album": "Rage Against the Machine",
    "release-date": 1992,
    "album-score": 879,
    "global-album-ranking": 4,
    "band-catalog-album-ranking": 1
  },
  {
    "id": 5,
    "name": "Soundgarden",
    "album": "Superunknown",
    "release-date": 1994,
    "album-score": 945,
    "global-album-ranking": 5,
    "band-catalog-album-ranking": 1
  },
  {
    "id": 6,
    "name": "The Beatles",
    "album": "Sgt. Pepper's Lonely Hearts Club Band",
    "release-date": 1967,
    "album-score": 800,
    "global-album-ranking": 1,
    "band-catalog-album-ranking": 1
  },
  {
    "id": 7,
    "name": "The Beatles",
    "album": "Abbey Road",
    "release-date": 1969,
    "album-score": 805,
    "global-album-ranking": 2,
    "band-catalog-album-ranking": 2
  }
]
```

### Return status

| Status value | Return status | Description |
| ------------- | ----------- | ----------- |
| 200 | Success | All albums retrieved successfully |
| ECONNREFUSED | N/A | Service is offline - start the service and try again |

---

## `GET`: retrieve an album by ID

Use the `/albums/{id}` endpoint to retrieve a specific album record
using the `GET` method.

### URL

```shell
{server_url}/albums/{id}
```

  When testing, the {server_url} is the local host:
  <http://localhost:3000/albums/{id}>.

### Path parameters

| Parameter | Type | Required | Description |
|-----------|------|----------|-------------|
| `id` | integer | Yes | The unique identifier of the album to retrieve |

### Request headers

| Header | Type | Required | Description |
|--------|------|----------|-------------|
| `Content-Type` | string | No | Not required for GET requests |

### Request body

No request body required for GET requests.

### Request syntax

```bash
curl -X GET http://localhost:3000/albums/{id}
```

### Response format

| Property name | Type | Description |
| ------------- | ----------- | ----------- |
| `id` | integer | Unique identifier assigned by the server |
| `name` | string | The band name |
| `album` | string | The album name |
| `release-date` | integer | The album release year |
| `album-score` | integer | The album score |
| `global-album-ranking` | integer | The global ranking of the album |
| `band-catalog-album-ranking` | integer | The ranking within the band's catalog |

### Request example

```bash
curl -X GET http://localhost:3000/albums/3
```

### Response example

```json
{
  "id": 3,
  "name": "Radiohead",
  "album": "Ok Computer",
  "release-date": 1997,
  "album-score": 955,
  "global-album-ranking": 3,
  "band-catalog-album-ranking": 1
}
```

### Return status

| Status value | Return status | Description |
| ------------- | ----------- | ----------- |
| 200 | Success | Album retrieved successfully |
| 404 | Error | Album with specified ID not found |
| ECONNREFUSED | N/A | Service is offline - start the service and try again |

---
