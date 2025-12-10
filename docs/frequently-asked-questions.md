---
# markdownlint-disable
# vale off
title: "Frequently Asked Questions"
layout: default
nav_order: 5
has_children: false
permalink: /frequently asked questions
has_toc: false
version: "v1.0"
last_updated: "2025-11-22"
# vale on
# markdownlint-enable
---
<!-- vale Google.Headings = NO -->

<!-- markdownlint-disable MD025 -->
<!-- markdownlint-disable MD033 -->
<!-- vale Google.Headings = NO -->
<!-- vale Google.Acronyms = NO -->
<!-- markdownlint-disable MD013 -->
<!-- vale Google.We = NO -->

<h1>
  <img src="./images/logo.png" alt="Rock-Rankers Logo" width="200" style="vertical-align: middle; margin-right: 10px;"/> Frequently asked questions
</h1>
<!-- markdownlint-enable MD025 MD033 -->
<!-- markdownlint-enable MD013 -->

## About Rock-Rankers

### 🎸 What's Rock-Rankers?

Rock-Rankers is a REST API that analyzes rock music using simple metrics. The
API ranks and compares bands, albums, and songs to create clear scores and
rankings.

### 🤘 Who created Rock-Rankers?
<!-- markdownlint-disable MD033 -->
<div style="display: flex; gap: 20px; align-items: center; margin-top: 30px;">
  <div style="flex: 1; text-align: center;">
    <img src="./images/Gill 2.jpg" alt="Gill" style="max-width: 75%; height: auto;">
  </div>
  <div style="flex: 1; font-size: 16px; padding: 0px 0px 0px 20px;">
    <h3 style="margin: 0 0 10px 0; font-size: 14px;">The Rock-Rankers story:</h3>
    The Rock-Rankers API grew out of a shared love of music.
<a href="https://GitHub.com/drenn08/">@drenn08</a> built the API, and
<a href="https://GitHub.com/GillWrites">@gillwrites</a> wrote the documentation.
We created this project as part of a learning program with the
University of Washington, which focuses on API documentation.
You can also check out our other music API project,
    <a href="https://github.com/drenn08/tune-guide-api">TuneGuide API</a>.
  </div>
</div>
<!-- markdownlint-enable MD033 -->

### Is Rock-Rankers a production API?

No. Rock-Rankers is a learning tool. It shows how REST APIs work and how to
document them. It uses a local JSON server to mimic real API calls

___

## Rock-Rankers evironnment

### 💻 Why does Rock-Rankers use a JSON environment?

Rock-Rankers uses JSON server to create a mock REST API from a JSON file.
This setup gives the following benefits:

- Quick to set up, no backend needed
- Works like a real API with GET, POST, PUT, PATCH, and DELETE
- Lets you test and learn with realistic API behavior
- Easy to change data and try new ideas
- Safe with no risk of breaking a production system

## 🔧 Troubleshooting

These are general troubleshooting tips. See the [tutorials](./tutorials.md)
and the [API reference docs](./api-referece-docs.md) troubleshooting sections
for steps on solving
specific issues.

<!-- vale Google.Acronyms = NO -->
<!-- vale Google.Headings = NO -->

### Server won't start

**Possible Causes:**

- Node.js or npm not installed
- Port 3000 already in use
- Wrong working directory
- JSON server not installed

**Solution:**

- Run `node --version` and `npm --version` to confirm they work
- Check if another app is using port 3000
- Make sure you are in the folder with the Rock-Rankers database file
- Make sure you installed JSON server correctly

### 404 not found error

**Possible Causes:**

- Wrong endpoint URL
- Missing or wrong resource ID
- Server not running
- Wrong port number

**Solution:**

- Check the URL for spelling errors
- Make sure the resource ID exists in the database
- Check that JSON server is running at `http://localhost:3000`
  
### 400 Bad Request error

**Possible Causes:**

- Invalid request body
- Missing required fields
- JSON syntax errors

**Solution:**

- Check that the request body uses valid JSON
- Include all required fields
- Check the JSON format: quotes, commas, and brackets

### POST, PUT, or PATCH requests fail

**Possible Causes:**

- Missing `Content-Type` header
- Invalid JSON format
- Wrong HTTP method
- Missing required fields

**Solution:**

- Add the `Content-Type: application/json` header
- Use valid JSON syntax in the request body
- Use POST to create, PUT to fully update, and PATCH to update part of a
  record
- Include all required fields

### ECONNREFUSED error

**Possible Causes:**

- JSON server not running
- Server crashed
- Wrong URL or port

**Solution:**

- Start JSON server with `json-server --watch rock-rankers-db.json`
- Check that JSON server is running at `http://localhost:3000`
- Look at the terminal for any error messages

___

### 🐙 How to contribute to Rock-Rankers

 We'd love your help. Whether you want to improve the docs, suggest features,  
or fix bugs, go to the Rock-Rankers GitHub repo:  

**[Rock-Rankers API on GitHub](https://github.com/GillWrites/rock-rankers-api)**
** [![GitHub Logo](./images/github-mark.png)](https://github.com/GillWrites/rock-rankers-api)

> 🐙 GitHub: [Open an issue](
> https://github.com/GillWrites/rock-rankers-api/issues)  
> → **Issues** → **New Issue**  
> Include a clear title, suggestions, what you tried, what happened.  
> Also include steps to reproduce, and your system info: OS and Node.js version.

## 📧 Need more help?

Reach out:
📧 email: [hello@rockrankers.com](mailto:hello@rockrankers.com)
