# ProMeta

The JSON Schema Definition for Project Metadata ".prometa" files.

## About

Have you ever took a sneak peek into someone's repo and couldn't confirm if it's an academic or commercial project, or if a new project that it's going to be maintained for long time or if it's just a POC that someone decided to put online just to prevent losing the code or to fill it's portfolio?

ProMeta is an upcoming JSON-based file that you can put in your repository with core metadata info about your project so people and tools can easily understand the project.

> The main goal is to simplify crawling and organize repositories using automation tools to display project's information elsewhere, like in a portfolio page.

### Example of a `.prometa` file

```json
{
  "prometa_version": "0.1.0",  // prometa schema version - default to latest
  "title": "ProMeta",  // Project title
  "description": "A project metadata file.",  // Project description
  "author": { "name": "Aaron Carneiro" },  // Can be authors: [] (array) or a single author (object)
  "source": "https://github.com/euaaron/prometa",  // Address to the project source code
  "hosting": {
    "name": "GitHub",  // Hosting service
    "public_url": "https://prometa.aaroncarneiro.com",  // Public address to access the project if it is a webapp or webservice.
  },
  "license": "CC0",
  "stability":  "experimental",
  "category": ["portfolio"],  // Project category, it can be Commercial, Learning, Portfolio, Prototype, Open-Source and others (you can use multiple)
  "keywords": ["schema", "tool", "metadata"]  // Additional keywords you would like to use to simplify searching
}
```

> A full definition can be seen in the prometa.schema.json.


## TODO

- [x] Create the Json Schema
- [ ] Setup this repo to accept contributions
- [ ] Create an extension for linting and hinting
  - [ ] for VSCode
  - [ ] for Visual Studio
  - [ ] for IntelliJ
  - [ ] for NeoVIM
- [ ] Create a CLI tool that
  - [ ] creates a `.prometa` file
  - [ ] verifies if a `.prometa` file is valid
  - [ ] automates filling some fields of `.prometa` files by reading `package.json`, `pom.xml`, `build.gradle`, `*.[cs|vb|fs]proj` and other languages.

## Author

[Aaron Carneiro](https://github.com/euaaron)
