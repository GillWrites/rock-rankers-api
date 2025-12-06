---
title: "API Reference Docs"
layout: default
nav_order: 4
has_children: true
permalink: /api-reference-docs
has_toc: false
version: "v1.0"
last_updated: "2025-09-03"
---

<!-- markdownlint-disable -->
<!-- vale off -->

<!-- vale on -->
<!-- markdownlint-enable -->

<!-- markdownlint-disable MD025 -->
<!-- markdownlint-disable MD033 -->
<!-- vale Google.Headings = NO -->
<!-- vale Google.Acronyms = NO -->
<!-- markdownlint-disable MD013 -->

<h1>
  <img src="./images/logo.png" alt="Rock-Rankers Logo" width="200" style="vertical-align: middle; margin-right: 10px;"/> API reference docs
</h1>
<!-- markdownlint-enable MD025 MD033 -->
<!-- markdownlint-enable MD013 -->

## 🎸 API endpoints

Rock-Rankers supports the full create, retrieve, update, and delete
**CRUD**  operation model for REST API design.

This reference provides details for all Rock-Rankers API endpoints. Use it to learn
how to create, retrieve, update, and delete data in the Rock-Rankers database.

Rock-Rankers has three main resources. Each one lets you create, read, update, and
delete data.

[**Bands Resource**](./API/bands.md) - Work with band data such as names,
genres, years active, and where the bands are from.

* [POST: create a new band](./API/post-band.md)
* [PUT: update an existing band](./API/put-band.md)
* [PATCH: partially update a band](./API/patch-band.md)
* [DELETE: delete a band](./API/delete-band.md)
  
[**Albums Resource**](./API/albums.md) - Work with album data like titles,
release dates, scores, and rankings.

* [POST: create a new album](./API/post-album.md)
* [PUT: update an existing album](./API/put-album.md)
* [PATCH: partially update an album](./API/patch-album.md)
* [DELETE: delete an album](./API/delete-album.md)

[**Users Resource**](./API/users.md) - Edit subscribers for the
Rock-Rankers platform.

* [POST: create a new user](./API/post-user.md)
* [PUT: update an existing user](./API/put-user.md)
* [PATCH: partially update a user](./API/patch-user.md)
* [DELETE: delete a user](./API/delete-user.md)

Each endpoint page shows you the request URL, HTTP method, parameters,
request body format, example requests, and sample responses. When you run
the local API server, all endpoints use the mock API base URL
<http://localhost:3000>.

---

## 🎸 Browse the Rock-Rankers OpenAPI spec  

🤘 **[Rock-Rankers OpenAPI Specification](https://raw.githubusercontent.com/GillWrites/rock-rankers-api/main/api/rock-rankers-spec.yml)**

The Rock-Rankers OpenAPI Specification shows best practices in REST API design
with these features:

**Complete Data Management** - Add, view, update, and delete users, bands, and
albums. Every action includes clear examples showing what to send and what you
get back.

**Helpful Error Messages** - When something goes wrong, you get clear error
messages that explain what happened and how to fix it, with tracking IDs to
help solve problems.

**Smart Data Handling** - Break large lists into pages, sort results by any
field, and update just the fields you need. Includes checks to make sure
emails, dates, and scores are valid.

**Works with Popular Tools** - Import into
[Postman](https://learning.postman.com/docs/sending-requests/requests/),
[Swagger UI](https://editor.swagger.io/), or other API tools to test the API
and generate code.

---

## Rock-Rankers on GitHub

View the source code, report issues, or help improve the project:

🎸 **[Rock-Rankers API on GitHub](https://github.com/GillWrites/rock-rankers-api)**
** [![GitHub Logo](./images/github-mark.png)](https://github.com/GillWrites/rock-rankers-api)

Found a bug or have a suggestion?
[Open an issue](https://github.com/GillWrites/rock-rankers-api/issues) on
GitHub.
