# Agent Commands

A community-driven collection of slash commands for AI coding assistants like [Cursor](https://cursor.com), [Windsurf](https://codeium.com/windsurf), and other AI-powered IDEs.

🌐 **Browse commands at [agentcmds.work](https://agentcmds.work)**

## What are Slash Commands?

Slash commands are reusable prompts that you can invoke in your AI coding assistant. Instead of typing the same instructions repeatedly, you save them as commands like `/deslop`, `/refactor`, or `/write-tests`.

## Contributing

We welcome contributions! See [CONTRIBUTING.md](CONTRIBUTING.md) for guidelines on adding new commands.

### Quick Start

1. Fork this repository
2. Create a new `.md` file in the `commands/` folder
3. Follow the [command template](CONTRIBUTING.md#command-template)
4. Submit a Pull Request

## Command Format

Each command is a Markdown file with YAML frontmatter:

```markdown
---
id: my-command
name: My Command Name
slug: my-command
category: code-quality
description: A brief description of what this command does.
---

Your command instructions go here...
```

### Required Fields

| Field         | Description                                                       |
| ------------- | ----------------------------------------------------------------- |
| `id`          | Unique identifier (lowercase, hyphens)                            |
| `name`        | Display name                                                      |
| `slug`        | URL-friendly identifier (usually same as id)                      |
| `category`    | One of: `code-quality`, `documentation`, `testing`, `refactoring` |
| `description` | Brief description (shown in command list)                         |

## Categories

- **code-quality** - Improve code quality, remove slop, fix issues
- **documentation** - Add or improve documentation
- **testing** - Write or improve tests
- **refactoring** - Restructure and improve code

## License

MIT License - feel free to use these commands in your projects!
