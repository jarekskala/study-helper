---
description: Create a commit message by analyzing git diffs
allowed-tools: Bash(git status:*), Bash(git add:*), Bash(git diff --staged), Bash(git commit:*)
---

## Context:

- Add current changes: !`git add -A`
- Current git status: !`git status`
- Current git diff: !`git diff --staged`

## Your task:

First stage all changes, then analyze them and create a commit message. Use present tense and explain "why" something has changed, not just "what" has changed.

## Commit types with emojis:

Only use the following emojis:

- ✨ `feat:` – New feature
- 🐛 `fix:` – Bug fix
- 🔨 `refactor:` – Refactoring code
- 📝 `docs:` – Documentation
- 🎨 `style:` – Styling/formatting
- ✅ `test:` – Tests
- ⚡ `perf:` – Performance
- 🔧 `chore:` – Chores / tooling / config / maintenance

## Language:

The commit message must be written in English.

## Format:

Use the following format for making the commit message:

```
<emoji> <type>: <concise_description>
<optional_body_explaining_why>
```

## Output:

1. Show summary of changes currently staged
2. Propose commit message with appropriate emoji
3. Ask for confirmation before committing

DO NOT auto-commit – wait for user approval, and only commit if the user says so.