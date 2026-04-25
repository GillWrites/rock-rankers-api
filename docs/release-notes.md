---
title: "Release Notes"
layout: default
nav_order: 6
has_children: false
permalink: /release-notes
has_toc: false
version: "v1.0"
last_updated: "2026-04-24"
description: "Release notes for the Rock Rankers API"
---

<!-- vale on -->
<!-- markdownlint-enable -->

## Release notes

Release notes for all versions of the Rock Rankers API.

---

### V1.1.0
<!-- vale Google.Colons = NO -->
**Release date:** April 24, 2026
<!-- vale Google.Colons = YES -->
#### New features
<!-- vale Google.Headings = NO -->
<!-- vale Google.Acronyms = NO -->
##### PUT method support for all resources
<!-- vale Google.Headings = YES -->
<!-- vale Google.Acronyms = YES -->

v1.1.0 adds `PUT` support to the `bands` and `albums` resources, completing
full `PUT` coverage across all three Rock Rankers API resources.

Use `PUT` to replace all properties of an existing resource in a single
request. Unlike `PATCH`, which supports partial updates, `PUT` requires a
complete request body.

The following endpoints now support `PUT`:

| Endpoint | Description |
| --- | --- |
| `PUT /bands/{id}` | Replaces all properties of an existing band. |
| `PUT /albums/{id}` | Replaces all properties of an existing album. |
| `PUT /users/{id}` | Replaces all properties of an existing user. |

---

### V1.0.0
<!-- vale Google.Colons = NO -->
**Release date:** December 12, 2025
<!-- vale Google.Colons = YES -->

#### Initial release

v1.0.0 is the initial release of the Rock Rankers API. This release
<!-- vale Google.Acronyms = NO -->
provides full CRUD support across three resources: `bands`, `albums`,
and `users`.
<!-- vale Google.Acronyms = YES -->
The following endpoints are available:

| Endpoint | Description |
| --- | --- |
| `GET /bands` | Returns a list of all bands. |
| `GET /bands/{id}` | Returns a single band by ID. |
| `POST /bands` | Creates a new band. |
| `PATCH /bands/{id}` | Partially updates an existing band. |
| `DELETE /bands/{id}` | Deletes a band by ID. |
| `GET /albums` | Returns a list of all albums. |
| `GET /albums/{id}` | Returns a single album by ID. |
| `POST /albums` | Creates a new album. |
| `PATCH /albums/{id}` | Partially updates an existing album. |
| `DELETE /albums/{id}` | Deletes an album by ID. |
| `GET /users` | Returns a list of all users. |
| `GET /users/{id}` | Returns a single user by ID. |
| `POST /users` | Creates a new user. |
| `PATCH /users/{id}` | Partially updates an existing user. |
| `DELETE /users/{id}` | Deletes a user by ID. |
