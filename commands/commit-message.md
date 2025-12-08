---
id: commit-message
name: Write Commit Message
slug: commit
category: documentation
description: Generate a Conventional Commit message from the current diff.
---
# Write Commit Message

Based on the current git diff, write a proper commit message following Conventional Commits format:

Format:
```
<type>(<scope>): <description>

[optional body]

[optional footer]
```

Types: feat, fix, docs, style, refactor, perf, test, chore

Guidelines:
- Subject line max 50 characters
- Use imperative mood ("add" not "added")
- Body should explain WHAT and WHY, not HOW
- Reference issue numbers if applicable

Analyze the diff and provide the commit message.

