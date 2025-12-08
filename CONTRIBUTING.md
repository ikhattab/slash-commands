# Contributing to Agent Commands

Thank you for contributing! This guide will help you add new commands or improve existing ones.

## Adding a New Command

### 1. Create the Command File

Create a new `.md` file in the `commands/` folder. The filename should match your command's slug (e.g., `my-command.md`).

### 2. Command Template

Use this template for your command:

```markdown
---
id: your-command-id
name: Your Command Name
slug: your-command-slug
category: code-quality
description: A concise description of what this command does.
---

# Your Command Title

Detailed instructions for the AI assistant go here.

Be specific about:

- What the AI should do
- What to look for
- What output format you expect
- Any constraints or guidelines
```

### 3. Field Guidelines

| Field         | Guidelines                                                             |
| ------------- | ---------------------------------------------------------------------- |
| `id`          | Lowercase, use hyphens, must be unique                                 |
| `name`        | Title case, descriptive but concise                                    |
| `slug`        | Same as `id` (used in URLs and `/command` invocation)                  |
| `category`    | Choose from: `code-quality`, `documentation`, `testing`, `refactoring` |
| `description` | One sentence, shown in command cards                                   |

### 4. Writing Good Commands

**DO:**

- Be specific and actionable
- Include examples of what to look for
- Specify the expected output format
- Keep instructions focused on one task

**DON'T:**

- Be too vague ("make it better")
- Include multiple unrelated tasks
- Assume context that won't be available
- Use placeholder text

### 5. Test Your Command

Before submitting:

1. Install the command in Cursor using the "Install in Cursor" button
2. Test it on real code
3. Verify it produces useful results

## Updating an Existing Command

1. Find the command file in `commands/`
2. Make your changes
3. Test the updated command
4. Submit a PR explaining what changed and why

## Categories

Choose the most appropriate category:

- **code-quality** - Improve code quality, remove AI slop, fix issues, security audits
- **documentation** - Add comments, docstrings, README content
- **testing** - Write unit tests, integration tests, test coverage
- **refactoring** - Restructure code, improve patterns, optimize

## Pull Request Process

1. Ensure your command follows the template
2. Test the command in Cursor
3. Fill out the PR template completely
4. Wait for review feedback

## Questions?

Open an issue if you have questions or need help!
