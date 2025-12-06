--- 
# markdownlint-disable
# Vale off
title: "API Reference Docs"
layout: default
nav_order: 4
has_children: true
permalink: /api-reference-docs
has_toc: false
version: "v1.0"
last_updated: "2025-09-03"
# Vale on
# markdownlint-enable
---

<!-- markdownlint-disable MD025 -->
<!-- markdownlint-disable MD033 -->
<!-- vale Google.Headings = NO -->
<h1>
  <img src="./images/logo.png" alt="Rock-Rankers Logo" width="200" style="vertical-align: middle; margin-right: 10px;"/> API reference docs
</h1>
<!-- markdownlint-enable MD025 MD033 -->

<!-- vale Google.Acronyms = NO -->

## API endpoints

This reference gives you complete details for all Rock-Rankers API endpoints. Use it to learn
how to create, retrieve, update, and delete data from the Rock-Rankers database.

Rock-Rankers has three main resources. Each one lets you create, read, update, and delete data:

[**Bands Resource**](./API/bands.md) - Work with rock band data like band names, genres, years active, and where
they're from. You can use POST, GET, PUT, PATCH, and DELETE methods.

[**Albums Resource**](./API/albums.md) - Work with album data like titles, release dates, scores, and rankings.
You can use POST, GET, PUT, PATCH, and DELETE methods.

[**Users Resource**](./API/users.md) - Work with user data for the Rock-Rankers platform. You can use POST, GET,
PUT, PATCH, and DELETE methods.

Each endpoint page shows you the request URL, HTTP method, parameters, request body format,
example requests, and sample responses. When you run the local API server, all endpoints use
the mock API base URL <http://localhost:3000>.

### Browse the rock-rankers-api repo and OpenAPI spec below

* [rock-rankers api repo](https://github.com/drenn08/rock-rankers-api)
* [OpenAPI Specification](https://raw.githubusercontent.com/GillWrites/rock-rankers-api/main/api/rock-rankers-spec.yml)
