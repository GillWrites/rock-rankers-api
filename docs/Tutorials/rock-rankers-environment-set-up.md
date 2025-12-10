---
# markdownlint-disable
# vale off
title: "Rock-Rankers quickstart tutorial"
parent: "Rock-Rankers quickstart"
layout: default
nav_order: 1
description: Describes how to configure your local computer to run a local instance of rock-rankers-api
permalink: /Rock-Rankers-quickstart/Rock-Rankers-quickstart-tutorial/
tags: 
    - get-started
categories: 
    - tutorials
ai_relevance: high
importance: 9
prerequisites: []
examples: []
api_endpoints: []
version: "v1.0"
last_updated: "2025-12-05"
# vale on
# markdownlint-enable
---

<!-- markdownlint-disable MD025 -->
<!-- markdownlint-disable MD033 -->
<!-- vale Google.Headings = NO -->
<!-- vale Google.Headings = NO -->
<div style="display: flex; align-items: center; margin-bottom: 20px;">
  <img src="/rock-rankers-api/images/logo.png"
       alt="Rock-Rankers Logo"
       width="200"
       style="margin-right: 20px; flex-shrink: 0;"/>
  <h1 style="margin: 0;">Rock-Rankers quickstart</h1>
</div>
<!-- vale Google.Headings = YES -->
<!-- markdownlint-enable MD025 MD033 -->

<!-- vale Google.Acronyms = NO -->
<!-- markdownlint-disable MD033 -->

## Follow these steps to get started using Rock-Rankers

* **[Build your Rock-Rankers development environment](#-build-your-rock-rankers-development-environment)**
* **[Verify your Rock-Rankers development environment](#-verify-your-rock-rankers-development-environment)**
* **[Make a test call to the Rock-Rankers service](#-make-a-test-call-to-the-rock-rankers-service)**

## 🤘 Build your Rock-Rankers development environment

Rock-Rankers uses a mock API server environment that acts like a real API. The mock API uses
JSON Server, which creates REST endpoints from your JSON data file. Following these steps
prepares your development system for a smooth Rock-Rankers experience.

Expect this preparation to take about 30 minutes to complete.

1. **Check prerequisites**
   * * Rock-rankers runs on any development system running a current version of Windows, macOS,
     or Linux.

2. **Install node.js**
      * Install [version 24.11.1 of `node.js`](https://nodejs.org/en/download).

3. **Install JSON server**
      * Install [version 0.17.4 of json-server](https://www.npmjs.com/package/json-server/v/0.17.4).
4. **Create a GitHub account**
      * Create a [GitHub cloud account](https://github.com).
  
5. **Create a fork of the Rock-Rankers API repository**
     * Browse to the
     [Rock-Rankers API repository](https://github.com/GillWrites/rock-rankers-api).
     * Create a fork of the Rock-Rankers repository within your GitHub account. This
     article tells you how: [Git: fork a repo](https://docs.github.com/articles/fork-a-repo).

6. **Install Git command line tools**
    * Follow this article to install Git command line.[Git: command line](https://docs.github.com/en/get-started/quickstart/set-up-git).

7. **Create a clone of forked Rock-Rankers API on GitHub Desktop**
   * [Install GitHub Desktop](https://desktop.github.com).
   * Create a clone of GitHub cloud's forked Rock-Rankers API on local GitHub Desktop. This article tells you how:
   [Cloning a GitHub repository](https://docs.github.com/en/desktop/adding-and-cloning-repositories/cloning-and-forking-repositories-from-github-desktop).
   * Create a branch from the Rock-Rankers main repository on your GitHub Desktop. This article
   tells you how, [Managing Branches in GitHub Desktop](https://docs.github.com/en/desktop/making-changes-in-a-branch/managing-branches-in-github-desktop).
   You'll run your Rock-Rankers tutorials from your branch.
  
<!-- vale Google.Acronyms = YES -->
<hr style="border: 0.5px solid grey;">

## 🤘 Verify your Rock-Rankers development environment

1. To test your development system, browse to your Rock-Rankers API repository.
   * Open a terminal and browse to your **GitHub repository workspace**. This is the
   directory that contains your fork of the **Rock-Rankers API** repository.

   ```shell
    cd <your GitHub repository workspace>/rock-rankers-api
   ```

   **For example:**

   ```shell
         cd /Documents/GitHub/GitHubRepos/rock-rankers-api
   ```

   Verify you are in the branch you created in step 7, [Build your Rock-Rankers development environment](#-build-your-rock-rankers-development-environment). Run the following command:

   ```shell
    git branch
   ```

   The current working branch has an asterisk *.

   **For example:**

   In the below example, the current working brancn is **quick-start-b**.

    ```shell
    MacBook-Air-3:rock-rankers-api gilliandeenihan$ git branch
    main
   * quick-start-b
 
   ```

2. Browse to the `/api` folder and verify you can see the JSON database.
The output should include the `rock-rankers-api.json` database.

```shell
 ls
 api-ranks-db-source.json
```

You are now ready to make a test call to the Rock-Rankers service.
<hr style="border: 0.5px solid grey;">

## 🤘 Make a test call to the Rock-Rankers service

1. Enter the following command to start the JSON server:

   ```shell
    json-server -w api-ranks-db-source.json
   ```

   If you installed the software correctly, you should see
   the service start and display the URL of the service: `http://localhost:3000`.

   <!-- vale Google.Exclamation = NO -->
   ```bash

   \{^_^}/ hi!

   Loading api-ranks-db-source.json
   Done

   Resources
   <http://localhost:3000/users>
   <http://localhost:3000/bands>
   <http://localhost:3000/albums>

   Home
   <http://localhost:3000>

   ```
   <!-- vale Google.Exclamation = YES -->

2. Open a second terminal. Make a test call to the Rock-Rankers service. This example makes a call to the resource
endpoint `bands`, to retrieve all band entries from the JSON database.

   ```shell
    curl http://localhost:3000/bands
   ```

If the service is running correctly, you should see a list of bands from the Rock-Rankers
database, such as in this example.

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

If you receive an error in any step of the procedure investigate. Correct the error before
continuing. Some common situations that cause errors include:

1. You mistyped a command.
2. You aren't in the correct directory.
3. A required software component didn't install correctly.
4. A required software component isn't up to date.

If you need more help, please email rock-rankers: <hello@rockrankers.com>
<hr style="border: 0.5px solid grey;">

## ➡️ Next steps

If you see the list of bands from the Rock-Rankers service, congratulations. You're ready to
move onto the next steps on your Rock-Rankers journey.

* **Try repeating this call using Postman**  
If you prefer visual tools over the command line, Postman is a great way to explore
Rock-Rankers without writing code. Learn how to install and use the [Postman desktop app](https://www.postman.com/downloads/).

* **Learn how to perform common Rock-Rankers tasks**  
 Hurrah, you are now ready to undertake Rock-Rankers [Tutorials](../tutorials.md) to learn how to query the Rock-Rankers database. Exceptional music search capabilities await. 🎸🤘
