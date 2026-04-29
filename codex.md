---
name: codex
description: Delegate a self-contained task to the Codex CLI to save tokens. Use when the user invokes /codex, or when explicitly asked to offload work to Codex. Good for file exploration, code reading, summarizing, and code generation that doesn't depend on the current conversation context.
---

# Codex Delegator

Run the task via Codex CLI instead of handling it yourself. Codex starts a fresh session with no conversation history, so it uses far fewer tokens for self-contained work.

## When to use

- User explicitly calls `/codex <task>`
- User says "use codex to..." or "let codex handle..."
- Self-contained tasks: reading files, exploring code, generating boilerplate, summarizing

## When NOT to use

- The task requires context from the current conversation
- The task involves editing files based on prior discussion
- The task needs your full understanding of what's been decided

## How to run

Use `codex exec` for non-interactive execution (plain `codex` requires a terminal):

```bash
codex exec "<task description>"
```

Return the output to the user as-is. No need to restate or summarize unless the output is very long, in which case highlight the key result.