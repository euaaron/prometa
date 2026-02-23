# ProMeta — VS Code Extension

Adds full editor support for [`.prometa`](https://github.com/euaaron/prometa) configuration files — repository-level project metadata in JSON format.

## Features

- **Schema validation** — real-time linting against the [ProMeta JSON Schema](https://github.com/euaaron/prometa/blob/v0.1.0/schema/prometa.json)
- **Autocomplete** — suggestions for all property names, enum values, and nested objects
- **Hover documentation** — descriptions for every field shown on hover
- **Error diagnostics** — highlights missing required fields (`title`, `description`, `source`, `license`), invalid types, and unknown properties

## How it works

The extension associates `*.prometa` files with VS Code language server.

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

## Required fields

| Field         | Type   | Description                                    |
| ------------- | ------ | ---------------------------------------------- |
| `title`       | string | Short project name                             |
| `description` | string | Short, objective description of the project    |
| `source`      | string | Canonical repository URL (e.g., GitHub)        |
| `license`     | string | License identifier (SPDX recommended)          |

## Optional fields

The schema also supports `author`/`authors`, `maintainers`, `website`, `category`, `keywords`, `class`, `compatibility`, `stability`, `related_projects`, `extensions`, `ci`, `learning`, `commercial`, `hosting`, and more. Use autocomplete (`Ctrl+Space`) inside a `.prometa` file to explore all available fields.

## Requirements

- VS Code 1.80 or later

## Links

- [ProMeta specification](https://github.com/euaaron/prometa)
- [ProMeta JSON Schema](https://github.com/euaaron/prometa/blob/v0.1.0/schema/prometa.json)
- [Report an issue](https://github.com/euaaron/prometa/issues)

## License

[CC0 1.0 Universal](LICENSE)
