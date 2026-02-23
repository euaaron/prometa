# ProMeta

The JSON Schema Definition for Project Metadata ".prometa" files.

## About

Have you ever took a sneak peek into someone's repo and couldn't confirm if it's an academic or commercial project, or if a new project that it's going to be maintained for long time or if it's just a POC that someone decided to put online just to prevent losing the code or to fill it's portfolio?

ProMeta is an upcoming JSON-based file that you can put in your repository with core metadata info about your project so people and tools can easily understand the project.

> The main goal is to simplify crawling and organize repositories using automation tools to display project's information elsewhere, like in a portfolio page.

## Example `.prometa` file

```json
{
  "title": "My Project",
  "description": "A short description of my project",
  "source": "https://github.com/user/my-project",
  "license": "MIT",
  "author": {
    "name": "Jane Doe",
    "email": "jane@example.com"
  },
  "category": "open-source",
  "class": "fullstack",
  "keywords": ["web", "typescript", "react"],
  "stability": "experimental"
}
```

### Required fields

| Field         | Type   | Description                                    |
| ------------- | ------ | ---------------------------------------------- |
| `title`       | string | Short project name                             |
| `description` | string | Short, objective description of the project    |
| `source`      | string | Canonical repository URL (e.g., GitHub)        |
| `license`     | string | License identifier (SPDX recommended)          |

### Optional fields

The schema also supports `author`/`authors`, `maintainers`, `website`, `category`, `keywords`, `class`, `compatibility`, `stability`, `related_projects`, `extensions`, `ci`, `learning`, `commercial`, `hosting`, and more. Use autocomplete (`Ctrl+Space`) inside a `.prometa` file to explore all available fields.


## TODO

- [x] Create the Json Schema
- [ ] Setup this repo to accept contributions
- [ ] Create an extension for linting and hinting
  - [x] for VSCode
  - [ ] for Visual Studio
  - [ ] for IntelliJ
  - [ ] for NeoVIM
- [ ] Create a CLI tool that
  - [ ] creates a `.prometa` file
  - [ ] verifies if a `.prometa` file is valid
  - [ ] automates filling some fields of `.prometa` files by reading `package.json`, `pom.xml`, `build.gradle`, `*.[cs|vb|fs]proj` and other languages.

## Author

[Aaron Carneiro](https://github.com/euaaron)
