<!-- vale Google.Headings = NO -->
# Rock Rankers API documentation
<!-- vale Google.Headings = YES -->

API documentation for the Rock Rankers REST API. Rock Rankers is a mock API that
aggregates
and visualizes rankings and scores for rock bands and albums.

Live documentation: <https://gillwrites.github.io/rock-rankers-api>

## Tech stack
<!-- vale Google.EmDash = NO -->
- [Jekyll](https://jekyllrb.com/) — static site generator
- [Just the Docs](https://just-the-docs.com/) — Jekyll documentation theme
- [JSON Server](https://www.npmjs.com/package/json-server/v/0.17.4) — mock
  REST API
- [GitHub Pages](https://pages.github.com/) — hosting
<!-- vale Google.EmDash = YES -->

## Run the API locally

### Prerequisites
<!-- vale Google.Acronyms = NO -->
- A current or LTS version of [Node.js](https://nodejs.org/en/download)
- [JSON Server v0.17.4](https://www.npmjs.com/package/json-server/v/0.17.4)
- A [GitHub account](https://github.com)
<!-- vale Google.Acronyms = YES -->
### Steps

1. Fork the repository on GitHub. For instructions, see
   [Fork a repo](https://docs.github.com/articles/fork-a-repo).

2. Clone your fork:

```shell
   git clone https://github.com/<your-github-username>/rock-rankers-api.git
```

1. Navigate to the API folder and start JSON Server:

```shell
   cd rock-rankers-api/api
   json-server --watch api-ranks-db-source.json
```

1. The API is now available at `http://localhost:3000`.

### Next steps

For a full walkthrough of setting up your environment and making your first
API request, see the
[Rock Rankers quickstart tutorial](https://gillwrites.github.io/rock-rankers-api/Rock-Rankers-quickstart/Rock-Rankers-quickstart-tutorial/).

## Project structure

```text
rock-rankers-api/
├── api/                        # JSON Server database and config
├── docs/                       # Documentation source files
│   ├── api-reference-docs/     # API reference pages
│   ├── tutorials/              # Tutorial pages
│   ├── release-notes.md        # Release notes
│   ├── faq.md                  # Frequently asked questions
│   └── contact.md              # Contact page
└── _config.yml                 # Jekyll configuration
```

## Author
<!-- vale Google.Spacing = NO -->
Gillian Deenihan
[gillwrites.GitHub.io/rock-rankers-api](https://gillwrites.github.io/rock-rankers-api)
<!-- vale Google.Spacing = YES -->