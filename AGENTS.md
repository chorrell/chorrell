# AGENTS.md - Agent Guidelines for This Repository

This repository contains a personal portfolio website for Christopher Horrell (DevOps Engineer).

## Project Overview

- **Type**: Static markdown-based portfolio website
- **Main content**: README.md with professional background, specializations, and contact info
- **Dependencies**: None (static site)

---

## Build / Lint / Test Commands

### Linting

Run markdownlint to check all markdown files:

```bash
docker run -v $PWD:/workdir davidanson/markdownlint-cli2:v0.5.1 "**/*.md" "#node_modules"
```

Or install markdownlint-cli2 globally and run:

```bash
markdownlint "**/*.md" "#node_modules"
```

### Running a Single Test

There are no test suites in this repository.

### GitHub Actions

The repository includes a CI workflow (`.github/workflows/markdownlint.yml`) that runs on pull requests.

---

## Code Style Guidelines

### Markdown Formatting

- **Line length**: No enforced limit (MD013 disabled in `.markdownlint.yaml`)
- **Inline HTML**: Allowed (MD033 disabled)
- Use ATX-style headers (`#`, `##`, `###`)
- Use fenced code blocks with language identifiers for code snippets
- Use blank lines between block elements

### File Naming

- Use lowercase with hyphens for any new markdown files
- Example: `getting-started.md`, `project-overview.md`

### Content Style

- Write in clear, concise English
- Use professional tone appropriate for a technical portfolio
- Include alt text for images: `![description](path/to/image.png)`
- Use relative paths for internal links

### Images

- Store images in the repository root or an `images/` directory
- Use descriptive, lowercase filenames with hyphens

### General Conventions

- Maximum one blank line between sections
- Use bullet points (`-`) for unordered lists
- Use numbers (`1.`) for ordered lists
- Wrap URLs in angle brackets if they're raw: `<https://example.com>`

---

## Error Handling

- Ensure all external links are valid (no broken URLs)
- Verify image paths exist before referencing them
- Check that relative links work from the file location

---

## Making Changes

1. Create a branch for your changes
2. Make edits following the style guidelines above
3. Run markdownlint before committing
4. Submit a pull request (CI will run linting automatically)

---

## Notes for Agents

- This is a simple static site - no build step required
- The only code in this repo is markdown and YAML (GitHub Actions)
- Focus on content quality and link correctness over complex formatting
- When adding new files, ensure they're markdown (`.md` extension)
