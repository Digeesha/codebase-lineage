# Codebase Lineage

Visualize your repository's evolution and uncover hidden code patterns

Codebase Lineage is a Git repository analysis tool that visualizes file evolution, tracks code ownership, and identifies refactoring hotspots across commit history. Developers and team leads use it to understand which files change together, who has expertise in specific modules, and where technical debt accumulates. The tool parses Git repositories, builds a relational model of commits, files, and authors, then presents interactive dashboards showing file churn rates, co-change patterns, and contributor impact over time.

## Features

- Upload and parse local Git repositories using JGit library
- Display commit timeline with filterable date ranges and author selection
- Show file churn heatmap identifying most frequently modified files
- Visualize co-change matrix revealing files that are modified together
- Generate contributor profiles with lines changed, commit frequency, and expertise areas
- Identify refactoring candidates based on high churn and multiple authors
- Export analysis reports as JSON or CSV for external tooling
- Persist repository metadata and analysis results in H2 database

## Tech stack

Java 17, Spring Boot, Thymeleaf, Maven, H2, JGit, H2 Database, Bootstrap, Chart.js

## How to run locally
### Prerequisites

- Java 17 or newer and Maven
### Environment variables


Copy `.env.example` to `.env` in the project root before starting the app.

**Windows**

```bash
copy .env.example .env
```

**macOS / Linux**

```bash
cp .env.example .env
```
From the project root:

```bash
mvn spring-boot:run
```

If the repo also has a frontend `package.json`, start that in a second terminal with `npm install` and `npm run dev`.

## Project structure

```
.
├── src/
├── .env.example
├── .gitignore
└── pom.xml
```

---

Generated with [Alviora AI](https://alvioraai.com).
