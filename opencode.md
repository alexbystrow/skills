---
name: opencode
description: Delegate a self-contained task to the OpenCode CLI to save tokens. Use when the user invokes /opencode, or when explicitly asked to offload work to OpenCode. Good for file exploration, code reading, summarizing, and code generation that doesn't depend on the current conversation context.
---

# OpenCode Delegator

Run the task via OpenCode CLI instead of handling it yourself. OpenCode starts a fresh session with no conversation history, so it uses far fewer tokens for self-contained work.

## When to use

- User explicitly calls `/opencode <task>`
- User says "use opencode to..." or "let opencode handle..."
- Self-contained tasks: reading files, exploring code, generating boilerplate, summarizing

## When NOT to use

- The task requires context from the current conversation
- The task involves editing files based on prior discussion
- The task needs your full understanding of what's been decided

## How to run

Pass the user's task directly to opencode:

```bash
opencode run "<task description>" 2>&1 | tail -n +2
```

The `tail -n +2` strips the first line (`Exporting session: ...` header).

Return the output to the user as-is. No need to restate or summarize unless the output is very long, in which case highlight the key result.
