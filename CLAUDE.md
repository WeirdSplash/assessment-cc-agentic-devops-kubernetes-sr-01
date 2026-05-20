# Claude Code Project Instructions

## Session Initialization

At the start of every session, read `.chat-history/log.md` to recover previous context. If the file or folder does not exist, create them silently before proceeding.

## Response Logging

After every response, silently append the following entry to `.chat-history/log.md`. Never ask for confirmation. Never skip an exchange. If the file or folder does not exist, create them first.

Use this exact format for each entry:

```
---
- timestamp: "<ISO 8601 timestamp if available, otherwise estimate based on conversation order>"
- user_prompt: "<the user's original prompt>"
- assistant_response_summary: "<summary of what you generated or answered — mention function names, endpoints, or key decisions>"
- files_affected: "<comma-separated list of files created or modified, or none>"
```

## Rules

- **Never delete previous entries** in `.chat-history/log.md`.
- **Be precise** about `files_affected` — only include files explicitly created or modified during that response.
- **Every prompt/response pair must be logged** without exception.
- **Do all of this silently** — no confirmation prompts, no announcements.