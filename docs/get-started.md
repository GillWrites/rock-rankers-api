---
# markdownlint-disable
# vale off
title: "Rock-Rankers Quickstart"
layout: default
nav_order: 2
has_children: true
permalink: /Rock-Rankers-Quickstart
has_toc: false
version: "v1.0"
last_updated: "2025-12-11"
# vale on
# markdownlint-enable
---

<!-- markdownlint-disable MD025 -->
<!-- markdownlint-disable MD033 -->
<!-- vale Google.Headings = NO -->
<h1>
  <img src="./images/logo.png" alt="Rock-Rankers Logo" width="200" style="vertical-align: middle; margin-right: 10px;"/> Rock-Rankers Quickstart
</h1>
<!-- markdownlint-enable MD025 MD033 -->

<!-- vale Google.Acronyms = NO -->

Explore Rock-Rankers with your own mock API server. Set up your local
environment and practice making API calls just like a real production API.

## How the Rock-Rankers mock API environment works

<!-- vale Google.Colons = NO -->
Rock-Rankers mock API server acts like a real API. The mock API uses
[JSON Server](https://www.npmjs.com/package/json-server/v/0.17.4),
which
creates REST endpoints from your JSON data file. The JSON server accepts standard
HTTP
requests:
[`GET`](https://developer.mozilla.org/en-US/docs/Web/HTTP/Reference/Methods/GET),
[`POST`](https://developer.mozilla.org/en-US/docs/Web/HTTP/Reference/Methods/POST),
[`PUT`](https://developer.mozilla.org/en-US/docs/Web/HTTP/Reference/Methods/PUT),
[`PATCH`](https://developer.mozilla.org/en-US/docs/Web/HTTP/Reference/Methods/PATCH),
and
[`DELETE`](https://developer.mozilla.org/en-US/docs/Web/HTTP/Reference/Methods/DELETE).
The server returns responses from your
local JSON database.
<!-- vale Google.Colons = YES -->

🤘 Ready to rock? Follow this tutorial to set up your Rock-Rankers environment
and make
your first API call.

🚀 [Rock-Rankers quickstart tutorial](./Tutorials/rock-rankers-environment-set-up.md)
