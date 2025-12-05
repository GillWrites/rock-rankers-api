---
title: "How to filter bands with combined query parameters"
layout: default
nav_order: 3
parent: "Tutorials"
has_children: false
permalink: /Tutorials/How-to-filter-bands-with-combined-query-parameters/
has_toc: false
description: "Tutorial outlining how to filter the `bands` endpoint using many query parameters"
tags:
  - api
categories:
  - tutorials
version: "v1.0"
last_updated: "2025-11-20"
---

<!-- markdownlint-disable MD025 -->
<!-- markdownlint-disable MD033 -->
<!-- vale Google.Headings = NO -->
<div style="display: flex; align-items: center; margin-bottom: 20px;">
  <img src="/rock-rankers-api/images/logo.png"
       alt="Rock-Rankers Logo"
       width="200"
       style="margin-right: 20px; flex-shrink: 0;"/>
  <h1 style="margin: 0;">How to filter bands with combined query parameters</h1>
</div>
<!-- vale Google.Headings = YES -->
<!-- markdownlint-enable MD025 MD033 -->

This tutorial shows how to query the Rock-Rankers database to get band data from
the `/bands` endpoint. The tutorial uses filters and query parameters. These filters search
bands by genre and origin.

This tutorial takes about 20 minutes to complete.

## 🚀 Before starting

Complete the [Rock-Rankers quickstart tutorial](./rock-rankers-environment-set-up.md) topic on
your development system before starting this tutorial.

## 🤘 Filter bands by genre and origin

The `GET` method uses the `_like` operator to filter band data from the `bands` resource.
The `_like` operator does partial text matching. This allows searches for bands that have
certain text in their fields.

1. Check that the local JSON server is running. Start the server with this command in the terminal, if needed.

   ```shell
   cd <your-github-workspace>/rock-rankers-api/api
   json-server --watch api-ranks-db-source.json
   ```

2. Open a second terminal. Run a `GET` command to the `bands` resource. Use combined query
   parameters with the `_like` operator.

   **Request syntax:**

   ```shell
   http://localhost:3000/bands?genre_like={genre}&origin_like={location}
   ```

   Note: replace {genre} with the genre to search for. Replace {location} with the origin
   location. The `_like` operator matches any band where the search text appears anywhere in
   the field.

   **Request example:**  
   This request queries the Rock-Rankers database. The request gets data about bands that have
   "rock" in their genre and "California" in their origin.

      ```shell
   curl "http://localhost:3000/bands?genre_like=rock&origin_like=California"
      ```

3. Check the response. The response returns only bands matching both filters.

```json
   [
     {
       "id": 4,
       "name": "Rage Against the Machine",
       "genre": "rock, alternative, metal, rap, funk",
       "years-active": "1991-2000; 2008-2011; 2019-2024",
       "origin": "Los Angeles, California, USA"
     }
   ]
```

### Understanding the `_like` operator

The `_like` operator works well with fields that have many values or long text. In this
example:

* `genre_like=rock` matches any band where "rock" appears in the genre field. This works even
  if the genre also has other styles like "alternative" or "metal."
* `origin_like=California` matches any band where "California" appears in the origin field.

When query parameters combine with `&`, the API returns only bands that match all the filters.

### Try different filter combinations

Try other filter combinations to explore the database:

**Example 1: find alternative bands from Seattle:**

```shell
curl "http://localhost:3000/bands?genre_like=alternative&origin_like=Seattle"
```

**Example 2: find bands from England:**

```shell
curl "http://localhost:3000/bands?origin_like=England"
```

**Example 3: find metal bands:**

```shell
curl "http://localhost:3000/bands?genre_like=metal"
```

## 🤘 What this tutorial covered

After completing this tutorial, you now know how to:

* Filter bands using combined query parameters.
* Use the `_like` operator to do partial text matching.
* Combine search filters to narrow down results from the rock-rankers database.

## 🔨 Troubleshooting

Refer to the table below if errors occur while following this tutorial:

| Status Code       | Problem                                        | Solution                                                                 |
|-------------------|------------------------------------------------|--------------------------------------------------------------------------|
| 200 OK            | Request successful                             | No action needed; the response contains the filtered band data           |
| 400 Bad Request   | Invalid query parameter format                 | Check that parameter names are correct, for example, `genre_like` not `genre-like`, and values are properly formatted |
| 404 Not Found     | No bands match the filter criteria             | Verify your filter values are correct; try broadening your search criteria or check that your database contains matching records |
| 500 Internal Server Error | json-server encountered an error       | Ensure json-server is running; restart it using `json-server --watch api-ranks-db-source.json` |
| ECONNREFUSED      | Can't connect to json-server                  | Verify json-server is running on port 3000; check that no other service is using the port |

## ➡️ Next steps

### Try more query combinations

Try more query combinations with curl to explore the API. Examples follow:

<!-- vale Google.Acronyms = NO -->
**Find grunge bands from the USA:**
<!-- vale Google.Acronyms = YES -->

```shell
curl "http://localhost:3000/bands?genre_like=grunge&origin_like=USA"
```

**Find blues bands from England:**

```shell
curl "http://localhost:3000/bands?genre_like=blue&origin_like=England"
```

**Find bands from Los Angeles:**

```shell
curl "http://localhost:3000/bands?origin_like=Los%20Angeles"
```

**Find alternative rock bands:**

```shell
curl "http://localhost:3000/bands?genre_like=alternative&genre_like=rock"
```

**Find bands from London:**

```shell
curl "http://localhost:3000/bands?origin_like=London"
```

### Try repeating this tutorial using Postman

Try these queries using the [Postman](https://learning.postman.com/docs/sending-requests/requests/)
GUI. Adapt the values from the tutorial to Postman's [**Params**](https://learning.postman.com/docs/sending-requests/create-requests/parameters/) section to make REST API calls.
Postman's **Params** allows adding many query parameters.
